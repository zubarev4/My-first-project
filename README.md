# Programos veikimas: 
1. _Patobulinimas_ Paleidus programą, vartotojo prašoma įvesti 1 - Generuoti failus.
2. _Patobulinimas_ Vartotojui sugeneruojami 5 failai su skirtingais studentų skaičiais: 1 000, 10 000, 100 000, 1 000 000, 10 000 000. Taip pat pateikiamas laikas, per kurį studentų failai buvo sukurti, nuskaityti, surūšiuoti ir išvesti į du naujus failus: viename paskirstyti visi studentai, kurių galutinis pažymis didesnis arba lygus 5 - kietekai, kitame studentai, kurių pažymis mažesnis nei 5 - vargšiukai.
3. Toliau vartotojo yra paklausiama, ar jis nori įvesti duomenis ar nuskaityti iš failo.
4. Jei pasirenkama, kad nuskaityti iš failo tai paklausiama iš kurio iš 4-ių failų norima nuskaityti.
5. Apskaičiavus rezultatus vartotojo paklausiama kaip jis norėtų rūšiuoti duomenis: vardas, pavardė, galutinis pagal vidurkį arba galutinis pagal medianą. 
6. Jei pasirenkama, kad įvesti duomenis tai paklausiama ar nori įvesti studento vardą bei pavardę ranka ar generuoti.
7. Paklausiama kokiu būdu norima įvesti pažymius (įrašyti ranka arba generuoti atsitiktinai).
8. Įrašius visus pažymius ir egzamino įvertinimą, vartotojui leidžiama pasirinkti pridėti dar studentų arba baigti žmonių įvedimą.
9. Pasirinkus vartotojui yra atspausdinamas sąrašas su visais studentais ir jų galutiniais vidurkiais ir medianomis.

1 tyrimas (darbas su failais): 
- Failų kūrimas:

![image](https://github.com/zubarev4/Pazymio-skaiciuokle/assets/147638474/99103d43-8344-4a5c-818c-d456aca2515d)

2 tyrimas, duomenų apdorijimas:
                     
                           1000 Studentų

|                       |                          | 
|-----------------------|-------------------------------|
| Skaitymas iš failo =  | 0.0036926s                         |
| Studentų rūšiavimas = | 0.0001938s                       |
| Studentų skirstymas = | 0.0005418s                       |
| Visos programos veikimo laikas = | 0.0044282s               | 

                                                 10000 Studentų

|                       |                         | 
|-----------------------|-------------------------------|
| Skaitymas iš failo =  | 0.0432751s                         |
| Studentų rūšiavimas = | 0.0016336s                       |
| Studentų skirstymas = | 0.0046939s                       |
| Visos programos veikimo laikas = | 0.0496026s               | 

                                                 100000 Studentų

|                       |                          | 
|-----------------------|-------------------------------|
| Skaitymas iš failo =  | 0.304183s                         |
| Studentų rūšiavimas = | 0.0221346s                       |
| Studentų skirstymas = | 0.065808s                       |
| Visos programos veikimo laikas = | 0.3921256s               | 
                                                 1000000 Studentų

|                       |                          | 
|-----------------------|-------------------------------|
| Skaitymas iš failo =  | 3.32989s                         |
| Studentų rūšiavimas = | 0.452937s                       |
| Studentų skirstymas = | 1.01328s                       |
| Visos programos veikimo laikas = | 4.796107s               | 
                                                 10000000 Studentų

|                       |                          | 
|-----------------------|-------------------------------|
| Skaitymas iš failo =  | 33.06s                         |
| Studentų rūšiavimas = | 3.24846s                       |
| Studentų skirstymas = | 7.13277s                       |
| Visos programos veikimo laikas = | 43.44123s               | 


