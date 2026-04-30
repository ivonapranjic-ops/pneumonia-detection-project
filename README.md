# strojno-ucenje-projekt
Diplomski studij Računarstvo, kolegij Strojno učenje
# Naslov projektnog zadatka: Detekcija upale pluća iz rendgenskih snimaka
Ovaj projekt fokusira se na klasifikaciju rendgenskih snimaka prsnog koša radi detekcije upale pluća. Cilj je bio usporediti performanse prilagođene VGG16 arhitekture (transfer learning) s jednostavnim baseline konvolucijskim modelom, uz poseban naglasak na interpretabilnost modela korištenjem Grad-CAM vizualizacije. 
# Ključne značajke:
- ARHITEKTURE: Implementacija i usporedba VGG16 (pre-trained) i custom baseline CNN-a.
- INTERPRETABILNOST: Korištenje Grad-CAM algoritma za vizualizaciju regija na slici koje su najviše utjecale na odluku modela (Explainable AI).
- PREDOBRADA PODATAKA: Korištenje CLAHE metode za poboljšanje kontrasta medicinskih snimaka (u aplikaciji).
- GUI: Razvijena interaktivna aplikacija korištenjem Streamlit biblioteke za jednostavno testiranje modela na novim slikama.

# Rezultati i metrike:
Modeli su evaluirani na testnom skupu od 624 slike. Poseban naglasak stavljen je na odziv i specifičnost zbog prirode medicinske dijagnostike (minimiziranje lažno negativnih rezultata). 

--- Rezultati na TESTNOM skupu za: Scratch CNN ---

Accuracy:    0.7468

Precision:   0.7125

Recall:      0.9974

F1 Score:    0.8312

Specificity: 0.3291


--- Rezultati na TESTNOM skupu za: VGG16 ---

Accuracy:    0.8670

Precision:   0.8344

Recall:      0.9821

F1 Score:    0.9022

Specificity: 0.6752


Napomena: Iako baseline ima visok recall, niska specifičnost ukazuje na to da model često klasificira zdrave pacijente kao bolesne. 

# Tehnologije:
- Jezik: Python
- PyTorch
- OpenCV, PIL
- Matplotlib, Seaborn
- Streamlit, Hugging Face

# Vizualizacija (Grad-CAM):
Projekt uključuje analizu "black box" problema kod neuronskih mreža. Kroz Grad-CAM je uočeno da model ponekad donosi odluke na temelju koštanih struktura (rebra, ključna kost) umjesto samog plućnog tkiva, što otvara prostor za daljnje istraživanje i poboljšanje. 

AUTOR: Ivona Pranjić
2025./2026.
