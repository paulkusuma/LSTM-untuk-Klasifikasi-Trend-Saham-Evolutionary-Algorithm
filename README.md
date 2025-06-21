# 📈 LSTM with Evolutionary Algorithm for Stock Trend Classification

Proyek ini merupakan implementasi model LSTM (Long Short-Term Memory) untuk melakukan klasifikasi tren harga saham Bitcoin (BTC-USD), yang dioptimalkan menggunakan Evolutionary Algorithm (EA). Proyek ini merupakan tugas Ujian Akhir Semester (UAS) dari Paul Wijaya Verda Kusuma - 215314051.

## 📚 Dependensi
Install semua dependensi dengan:
```bash
pip install numpy pandas scikit-learn tensorflow joblib deap

📁 Struktur Data

Data input berasal dari file BTC-USD_processed_data.csv dan memuat data historis BTC/USD. Fitur tambahan teknikal yang digunakan antara lain:

    MA5, MA10 (Moving Averages)

    ROC5 (Rate of Change)

    RSI (Relative Strength Index)

    EMA10, MACD, MACD Signal

    Bollinger Bands (Upper, Lower)

    ATR (Average True Range)

🔁 Preprocessing

    Scaling dilakukan dengan MinMaxScaler.

    Fitur-fitur teknikal ditambahkan secara manual.

    Label target didefinisikan berdasarkan perubahan harga.

🧠 Model

    Menggunakan model LSTM berlapis: LSTM → Dropout → Dense.

    Loss function: binary_crossentropy

    Optimizer: Adam (dioptimasi EA)

🧬 Evolutionary Algorithm (EA)

EA digunakan untuk mencari konfigurasi hiperparameter terbaik (seperti jumlah unit, dropout rate, batch size, dsb) dari model LSTM.

    Library: DEAP

    Proses: selection, crossover, mutation

    Evaluasi: menggunakan akurasi validasi

📊 Evaluasi

Model dievaluasi menggunakan:

    Confusion Matrix

    Classification Report (Precision, Recall, F1)

📦 Output

    Model LSTM yang terlatih

    File scaler tersimpan: scaler_btc_usd.pkl
