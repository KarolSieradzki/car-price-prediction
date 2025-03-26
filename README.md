# Projekt analizy i predykcji cen samochodów

## Spis treści
1. [Wstęp](#wstęp)
2. [Czyszczenie danych](#czyszczenie-danych)
3. [Eksploracyjna analiza danych (EDA)](#eksploracyjna-analiza-danych-eda)
4. [Inżynieria cech](#inżynieria-cech)
5. [Modelowanie](#modelowanie)

## Wstęp

Projekt miał na celu analizę i predykcję cen samochodów na podstawie różnych cech pojazdów. Wykorzystano w nim techniki czyszczenia danych, eksploracyjnej analizy danych (EDA), inżynierii cech oraz zaawansowane metody uczenia maszynowego.

## Czyszczenie danych

W pierwszym etapie projektu skupiono się na przygotowaniu i oczyszczeniu danych:

1. Usunięto niepotrzebne kolumny, które nie wnosiły wartości do analizy.
2. Zidentyfikowano i usunięto wiersze z brakującymi wartościami, gdy stanowiły one znaczący procent danych.
3. Dla kolumn z niewielką liczbą brakujących wartości, zastosowano imputację medianą.
4. Sprawdzono i usunięto ewentualne duplikaty.
5. Ujednolicono formaty danych, np. konwertując daty do odpowiedniego formatu.

## Eksploracyjna analiza danych (EDA)

W ramach EDA przeprowadzono następujące analizy:

1. Zbadano rozkłady zmiennych numerycznych, wykorzystując histogramy i wykresy pudełkowe.
2. Przeanalizowano zmienne kategoryczne, tworząc wykresy słupkowe pokazujące częstość występowania poszczególnych kategorii.
3. Sprawdzono korelacje między zmiennymi numerycznymi, używając macierzy korelacji i map cieplnych.
4. Zidentyfikowano potencjalne wartości odstające i rozważono ich wpływ na model.
5. Przeanalizowano zależności między ceną a kluczowymi zmiennymi, takimi jak przebieg, rok produkcji czy marka pojazdu.

## Inżynieria cech

W celu poprawy jakości modelu, stworzono 24 nowe cechy:

1. Wiek pojazdu (na podstawie roku produkcji).
2. Przebieg roczny (przebieg podzielony przez wiek pojazdu).
3. Moc na litr pojemności silnika.
4. Stosunek przebiegu do mocy.
5. Połączone cechy, np. marka i model pojazdu.
6. Wskaźniki dla różnych kategorii wyposażenia (bezpieczeństwo, komfort, technologia).
7. Logarytmy niektórych zmiennych numerycznych (np. przebieg, moc, pojemność).
8. Zmienne binarne dla pierwszego właściciela i stanu pojazdu.

Dodatkowo, przeprowadzono analizę unikalności danych kategorycznych, co pomogło w identyfikacji potencjalnych problemów z kodowaniem tych zmiennych.

## Modelowanie

Do modelowania wykorzystano algorytm CatBoost, który jest szczególnie efektywny w pracy z danymi kategorycznymi:

1. Podzielono dane na zbiory treningowy i walidacyjny.
2. Zastosowano bibliotekę Optuna do optymalizacji hiperparametrów modelu CatBoost.
3. Wytrenowano model na zoptymalizowanych parametrach.
4. Oceniono wydajność modelu, używając metryk takich jak RMSE i R2.
5. Przeprowadzono analizę ważności cech, aby zrozumieć, które zmienne mają największy wpływ na predykcję ceny.
