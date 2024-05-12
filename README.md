# Programos veikimas: 
1. Paleidus programą, vartotojo prašoma įvesti 1 - Generuoti failus.
2. Vartotojui sugeneruojami 5 failai su skirtingais studentų skaičiais: 1 000, 10 000, 100 000, 1 000 000, 10 000 000. Taip pat pateikiamas laikas, per kurį studentų failai buvo sukurti, nuskaityti, surūšiuoti ir išvesti į du naujus failus: viename paskirstyti visi studentai, kurių galutinis pažymis didesnis arba lygus 5 - kietekai, kitame studentai, kurių pažymis mažesnis nei 5 - vargšiukai.
3. Toliau vartotojo yra paklausiama, ar jis nori įvesti duomenis ar nuskaityti iš failo.
4. Jei pasirenkama, kad nuskaityti iš failo tai paklausiama iš kurio iš 4-ių failų norima nuskaityti.
5. Apskaičiavus rezultatus vartotojo paklausiama kaip jis norėtų rūšiuoti duomenis: vardas, pavardė, galutinis pagal vidurkį arba galutinis pagal medianą. 
6. Jei pasirenkama, kad įvesti duomenis tai paklausiama ar nori įvesti studento vardą bei pavardę ranka ar generuoti.
7. Paklausiama kokiu būdu norima įvesti pažymius (įrašyti ranka arba generuoti atsitiktinai).
8. Įrašius visus pažymius ir egzamino įvertinimą, vartotojui leidžiama pasirinkti pridėti dar studentų arba baigti žmonių įvedimą.
9. Pasirinkus vartotojui yra atspausdinamas sąrašas su visais studentais ir jų galutiniais vidurkiais ir medianomis.


### Instaliavimo instrukcija
- Jeigu naudojate „Visual Studio Code“, rekomenduojama įdiegti šiuos išplėtinius:
"C/C++ Extension Pack", "C/C++ Runner", "Code Runner".
- Taip pat parsisiuskite https://www.msys2.org/ ir nusistatykite bin folderį į PATH per environmental variables.
- Meniu juostos pasirinkite "Terminal“ -> "Select Default Profile“. Šiame lange turėtumete rasti bash(MSYS2) C:\msys64\usr\bin\bash.exe.
Naudodami cd komandą, pateikite klonuoto saugyklos kelią: cd jūsų/direktorijos/kelias/
Pavyzdžiui, cd /c/ISI/1k/2s/Objektinis\ programavimas/v1.0
- Norėdami paleisti programą, turite ją sukompiliuoti naudodami „Makefile“ failą, kuris yra saugykloje. Programos (pvz., VSCode) terminale rašykite:
make
./run


### Naudojami sistemos parametrai
- CPU 11th Gen Intel(R) Core(TM) i7-1165G7 @ 2.80GHz Cores:	4 Logical processors:	8
- RAM 16GB
- HDD TOSHIBA MQ04ABF100 Capacity:	932 GB
- SDD PC SN530 NVMe WDC 512GB Capacity:	477 GB

# v0.1
- C versija veikia tik su C masyvais.
- std::vector versija veikia tik su std::vector konteineriais.
- Yra meniu skirtingos programos eigos pasirinkimui.

# v0.2
- Rezultatų failai duomenys pateikinėja atitinkamai pagal vardą pavardę ir galutinį pažymį, bei rūšiuojami pagal naudotojo parinktą parametrą.  
- Testavimas atliekamas su iš anksčiau sugeneruotais failais (tyrimo patikimumui) ir pateiktas kelių testų laikų vidurkis. 

# v0.3
- Programa tikrina naudojant klaidų gaudymo mechanizmą ar failas egzistuoja nurodytoje vietoje. 
- Programoje turi būti realizuoti duomenų įvesties tikrinimai naudojant klaidų gaudymo mechanizmą.
- Pridėti antraštinis (*.h) failas vektoriai.h ir naujas vektoriai.cpp failas.

# v0.4
- Kuriami atskiri konteineriai geriems ir nepažangiems studentams, atliekamas jų rušiavimas prieš išvedant juos į failus pagal naudotojo parinktą parametrą. 
- Testavimas atliekamas su iš anksčiau sugeneruotais failais (tyrimo patikimumui!!!) ir pateiktas kelių testų laikų vidurkis.


# v1.0
- *Pridėtos dvi kodo variacijos (Vienoje yra naudojamas deque, kitoje list)* 
- *Pridėtos trys studentų skirstymo strategijos 1, 2 ir 3:*
## 1 Strategija
Bendro studentai konteinerio (vector, list ir deque tipų) skaidymas (rūšiavimas) į du naujus to paties tipo konteinerius: "vargšiukų" ir "kietiakų".
                                                  1000 Studentų

|                       | Vector                     | List                          | Deque                         |
|-----------------------|----------------------------|-------------------------------|-------------------------------|
| Skaitymas iš failo =  | 0.0036926s                    | 0.0149081s                       | 0.00528s                        |
| Studentų rūšiavimas = | 0.0001938s                    | 0.0001335s                            | 0.000794s                       |
| Studentų skirstymas = | 0.0005418s                    | 0.0012544s                       | 0.005222s                       |

                                                 10000 Studentų

|                       | Vector                        | List                          | Deque                         |
|-----------------------|-------------------------------|-------------------------------|-------------------------------|
| Skaitymas iš failo =  | 0.0432751s                       | 0.0656312s                       | 0.049548s                        |
| Studentų rūšiavimas = | 0.0016336s                       | 0.0022995s                        | 0.007361s                       |
| Studentų skirstymas = | 0.0046939s                       | 0.0128055s                       | 0.032534s                       |

                                                 100000 Studentų

|                       | Vector                        | List                          | Deque                         |
|-----------------------|-------------------------------|-------------------------------|-------------------------------|
| Skaitymas iš failo =  | 0.304183s                        | 0.524015s                        | 0.55426s                        |
| Studentų rūšiavimas = | 0.0221346s                       | 0.0587081s                       | 0.077897s                       |
| Studentų skirstymas = | 0.065808s                       | 0.168365s                       | 0.317550s                        |

                                                 1000000 Studentų

|                       | Vector                        | List                          | Deque                         |
|-----------------------|-------------------------------|-------------------------------|-------------------------------|
| Skaitymas iš failo =  | 3.32989s                         | 5.39987s                       | 4.874854s                       |
| Studentų rūšiavimas = | 0.452937s                       | 0.813123s                       | 0.881575s                       |
| Studentų skirstymas = | 1.01328s                       | 1.93492s                       | 2.765698s                       |

                                                 10000000 Studentų

|                       | Vector                        | List                          | Deque                         |
|-----------------------|-------------------------------|-------------------------------|-------------------------------|
| Skaitymas iš failo =  | 33.06s                       | 55.6257s                      | 28.129s                      |
| Studentų rūšiavimas = | 3.24846s                       | 12.1153s                      | 25.0634s                       |
| Studentų skirstymas = | 7.13277s                       | 39.32s                       | 54.2685s                      |

## 2 Strategijos tyrimai
Bendro studentų konteinerio (vector, list ir deque) skaidymas (rūšiavimas) panaudojant tik vieną naują konteinerį: "vargšiukai". 

                                                 1000 Studentų

|                       | Vector                     | List                          | Deque                         |
|-----------------------|----------------------------|-------------------------------|-------------------------------|
| Skaitymas iš failo =  | 0.0119565s                    | 0.0211578s                       | 0.00511s                        |
| Studentų rūšiavimas = | 0.0002629s                    | 0.0001297s                            | 0.0007789s                       |
| Studentų skirstymas = | 0.00146s                    | 0.0010577s                       | 0.005258s                       |

                                                 10000 Studentų

|                       | Vector                        | List                          | Deque                         |
|-----------------------|-------------------------------|-------------------------------|-------------------------------|
| Skaitymas iš failo =  | 0.0446615s                       | 0.0675249s                       | 0.085395s                        |
| Studentų rūšiavimas = | 0.0015341s                       | 0.0025594s                        | 0.007591s                       |
| Studentų skirstymas = | 0.0891403s                       | 0.0081296s                       | 0.036534s                       |

                                                 100000 Studentų

|                       | Vector                        | List                          | Deque                         |
|-----------------------|-------------------------------|-------------------------------|-------------------------------|
| Skaitymas iš failo =  | 0.309358s                        | 0.535423s                        | 0.726896s                        |
| Studentų rūšiavimas = | 0.0220498s                       | 0.0515397s                       | 0.0774757s                       |
| Studentų skirstymas = | 9.70369s                       | 0.122831s                       | 0.314180s                        |

                                                 1000000 Studentų

|                       | Vector                        | List                          | Deque                         |
|-----------------------|-------------------------------|-------------------------------|-------------------------------|
| Skaitymas iš failo =  | 1.50279s                         | 5.91206s                       | 6.87248s                       |
| Studentų rūšiavimas = | 0.138045s                       | 0.772712s                       | 0.88415s                       |
| Studentų skirstymas = | 219.803s                       | 1.47556s                       | 2.76756s                       |

                                                 10000000 Studentų

|                       | Vector                        | List                          | Deque                         |
|-----------------------|-------------------------------|-------------------------------|-------------------------------|
| Skaitymas iš failo =  | 11.6856s                       | 54.0294s                      | 28.0563s                      |
| Studentų rūšiavimas = | 1.11208s                       | 12.2951s                      | 24.4709s                       |
| Studentų skirstymas = | 308.112s                       | 19.0103s                       | 51.2097s                      |

## 3 Strategijos tyrimai
Bendro studentų konteinerio skaidymas, naudojant 1 ar 2 strategiją ir įtraukiant "efektyvius" darbo su konteineriais metodus.
                                                 1000 Studentų

|                       | Vector                     | List                          | Deque                         |
|-----------------------|----------------------------|-------------------------------|-------------------------------|
| Skaitymas iš failo =  | 0.0025374s                    | 0.0144695s                       | 0.0039819s                        |
| Studentų rūšiavimas = | 0.0002483s                    | 0.0001675s                            | 0.000643s                       |
| Studentų skirstymas = | 0.0008366s                    | 0.0010113s                       | 0.0011291s                       |

                                                 10000 Studentų

|                       | Vector                        | List                          | Deque                         |
|-----------------------|-------------------------------|-------------------------------|-------------------------------|
| Skaitymas iš failo =  | 0.0277175s                       | 0.0536126s                       | 0.0284664s                        |
| Studentų rūšiavimas = | 0.0023885s                       | 0.0023832s                        | 0.0113824s                       |
| Studentų skirstymas = | 0.0053708s                       | 0.0083332s                       | 0.0158623s                       |

                                                 100000 Studentų

|                       | Vector                        | List                          | Deque                         |
|-----------------------|-------------------------------|-------------------------------|-------------------------------|
| Skaitymas iš failo =  | 0.276704s                        | 0.521458s                        | 0.278395s                        |
| Studentų rūšiavimas = | 0.0221133s                       | 0.0536415s                       | 0.139493s                       |
| Studentų skirstymas = | 0.0479825s                       | 0.140012s                       | 0.183504s                        |

                                                 1000000 Studentų

|                       | Vector                        | List                          | Deque                         |
|-----------------------|-------------------------------|-------------------------------|-------------------------------|
| Skaitymas iš failo =  | 4.72s                         | 5.34137s                       | 3.05556s                       |
| Studentų rūšiavimas = | 0.3307s                       | 0.891866s                       | 1.96961s                       |
| Studentų skirstymas = | 0.8901s                       | 1.72001s                       | 2.40986s                       |

                                                 10000000 Studentų

|                       | Vector                        | List                          | Deque                         |
|-----------------------|-------------------------------|-------------------------------|-------------------------------|
| Skaitymas iš failo =  | 10.0641s                       | 53.1932s                      | 26.8887s                      |
| Studentų rūšiavimas = | 1.10318s                       | 12.5285s                      | 25.4083s                       |
| Studentų skirstymas = | 1.91224s                       | 21.6124s                       | 33.7335s                      |

