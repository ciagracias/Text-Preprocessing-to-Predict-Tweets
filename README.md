# Text Preprocessing to Predict Tweets
Sebelum memprediksi / menganilisis data, perlu dilakukan tahapan preprocessing yang bertujuan untuk memastikan bahwa data yang akan digunakan untuk analisis memiliki kualitas yang baik sehingga model yang dibangun akan menghasilkan akurasi dan klasifikasi yang baik pula.

Dataset yang akan digunakan untuk melakukan text preprocessing berupa 10000 data tweet yang terbagi menjadi dua kelas yaitu data yang mengandung kata - kata tidak pantas dan data normal.

Sumber : https://www.kaggle.com/competitions/nlp-getting-started/data

Beberapa tahapan yang dilakukan pada saat text preprocessing, diantaranya:
1. Lower Text
2. Missing Value
3. Removal of URLs
4. Chat Words Conversion
5. Removal of Punctuations
6. Removal of Stopwords
7. Removal of Frequent Words
8. Removal of Rare Words
9. Stemming
10. Lemmatization

#### 🌟LOWER TEXT 
Berguna untuk mengubah seluruh teks yang dipanggil menjadi huruf kecil.
<table>
  <tr>
    <td align="center">
      Sebelum Diproses
    </td>
    <td align="center">
      Setelah Diproses
    </td>
  </tr>
  <tr>
    <td>
      @aria_ahray @The Tawniest The out of control wild fires in California even in the Northen part of state. Very troubling.
    </td>
    <td>
      @aria_ahray @the tawniest the out of control wild fires in California even in the northen part of state. very troubling.
    </td>
  </tr>
  <tr>
    <td>
      The Latest: More Homes Razed by Northern California Wildfire - ABC News http://t.co/YmY4rSkQ3d
    </td>
    <td>
      the latest: more homes razed by northern california wildfire - abc news http://t.co/ymy4rskq3d
    </td>
  </tr>
</table>

#### 🌟MISSING VALUE 
Berguna untuk mengecek apakah terdapat data yang hilang atau tidak. Apabila ada data yang hilang maka dapat diatasi dengan beberapa cara, salah satunya adalah melakukan replace pada data yang hilang. Pada dataset, terdapat 61 data hilang pada kolom keyword dan 2533 data hilang pada kolom location.
<table>
  <tr>
    <td align="center">
      Keyword (Sebelum handling missing value)
    </td>
    <td align="center">
      Keyword (Setelah handling missing value)
    </td>
  </tr>
  <tr>
    <td>
      NaN
    </td>
    <td>
      No Keyword
    </td>
  </tr>
</table>

#### 🌟REMOVAL OF URLS 
Berguna untuk menghapus alamat website yang ada di dalam teks.
<table>
  <tr>
    <td align="center">
      Sebelum Diproses
    </td>
    <td align="center">
      Setelah Diproses
    </td>
  </tr>
  <tr>
    <td>
      The Latest: More Homes Razed by Northern California Wildfire - ABC News http://t.co/YmY4rSkQ3d
    </td>
    <td>
      the latest: more homes razed by northern california wildfire - abc news 
    </td>
  </tr>
</table>

#### 🌟CHAT WORDS CONVERSION 
Pengguna tweet umumnya banyak menggunakan kata yang disingkat sehingga proses ini akan berguna untuk memperluas kata - kata tersebut. Daftar kata yang disingkat dapat disimpan pada variabel chat_word.
<table>
  <tr>
    <td align="center">
      Sebelum Diproses
    </td>
    <td align="center">
      Setelah Diproses
    </td>
  </tr>
  <tr>
    <td>
      Horrible Accident Man Died In Wings Of Â‰Ã›ÃAirplaneÂ‰Ã›Â 29-07-2015. WTF You CanÂ‰Ã›Âªt Believe Your EYES Â‰Ã›Ã’... http://t.co/6fFyLAjWpS,1
    </td>
    <td>
      horrible accident man died in wings of  Â‰Ã›ÃairplaneÂ‰Ã›Â 29-07-2015. what the fuck you canÂ‰Ã›Âªt believe your eyes Â‰Ã›Ã’... 
    </td>
  </tr>
</table>

#### 🌟REMOVAL OF PUNCTUATIONS 
Berguna untuk menghapus tanda baca atau simbol - simbol tertentu yang ada pada teks.
<table>
  <tr>
    <td align="center">
      Sebelum Diproses
    </td>
    <td align="center">
      Setelah Diproses
    </td>
  </tr>
  <tr>
    <td>
      M1.94 [01:04 UTC]?5km S of Volcano Hawaii. http://t.co/zDtoyd8EbJ
    </td>
    <td>
      m194 0104 utc5km s of volcano hawaii
    </td>
  </tr>
</table>

#### 🌟REMOVAL OF STOPWORDS 
Berguna untuk menghapus kata - kata yang tidak begitu penting atau tidak memberikan informasi berharga pada saat analisis data.
<table>
  <tr>
    <td align="center">
      Sebelum Diproses
    </td>
    <td align="center">
      Setelah Diproses
    </td>
  </tr>
  <tr>
    <td>
      Strict liability in the context of an airplane accident - http://t.co/gibyQHhKpk,1
    </td>
    <td>
      strict liability context airplane accident
    </td>
  </tr>
</table>
