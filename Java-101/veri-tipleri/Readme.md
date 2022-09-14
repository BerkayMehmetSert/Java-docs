## Java Veri Tipleri 

Veri Tipleri (tür) bir değişkenin bellekte kaç byte yer kapladığını belirten kavramdır. Veri tipleri, değişkenlerin hafızada hangi aralıkta ve nasıl bir formatta tutulduğunu belirtir. 

Java'da iki tip değişken grubu vardır:
- İlkel Veri Tipleri (Primitive Data Types)
- Nesne Veri Tipleri (Object Data Types ya da Non-Primitive Data Types)

### İlkel Veri Tipleri (Primitive Data Types)

Java'da dille birlikte tanımlı olarak gelen 8 adet ilkel veri tipi vardır.
- boolean
- int
- char
- byte
- short
- long
- float
- double

| **Veri Tipi** | **Varsayılan Değeri** | **Veri Boyutu** |        **Sınırlı Değerler**                     |
| ------------- | --------------------- | --------------- | ----------------------------------------------  |
| boolean       | false                 | 1 bit           | true, false                                     |
| char          | &#39;\u0000&#39;      | 2 byte          | [0, +65635]                                     |
| byte          | 0                     | 1 byte          | [-128, +127]                                    |
| short         | 0                     | 2 byte          | [-32768, +32767]                                |
| int           | 0                     | 4 byte          | [-2147483648, +2147483647]                      |
| long          | 0L                    | 8 byte          | [-9223372036854775808, +9223372036854775807]    |
| float         | 0.0f                  | 4 byte          | [+-3.6 * 10^-38, +-3.6 * 10^+38]                |
| double        | 0.0d                  | 8 byte          | [+-1.8 * 10^-308, +-1.8 * 10^+308]              |

#### "boolean" Veri Tipi

Bu veri tipinde sadece iki deper tutabiliriz. "true" ya da "false" şeklinde iki değere sahiptirç Hafızada 1 Bit büyüklüğünde yer kaplar.

Örnek Tanımlama:

```java
boolean isTrue = true;
boolean isFalse = false;
```

#### "byte" Veri Tipi

-128 ile 127 arasında değer alabilen sayısal bir tam sayı tipidir. Varsayılan değeri 0'dır. Özellikle, hafızada az yer kaplaması nedeniyle kullanılabilir. Eğer, "int" tipine gerek duymuyorsanız, "byte" kullanmak faydalı olacaktır.

Örnek Tanımlama:

```java
byte b1 = 127;
byte b2 = -128;
```

#### "short" Veri Tipi

16 Bit'lik (yani 2 Byte) veri büyüklüğüne sahip tam sayı veri tipidir.  -32,768 ile 32,767 arasında değer alabilir. Varsayılan değeri sıfırdır. Yine "int" veri tipine ihtiyaç duymadığınız zaman "short" tipte değişkenler oluşturarak hafızada yer tasarrufu sağlayabilirsiniz.

Örnek Tanımlama:

```java
short s1 = 32767;
short s2 = -32768;
```

#### "int" Veri Tipi

32 Bit'lik (yani 4 Byte) veri büyüklüğüne sahip tam sayı veri tipidir. -2,147,483,648 ile 2,147,483,647 arasında değer alabilir. Varsayılan değeri sıfırdır. Bu veri tipi, genellikle sayısal işlemlerde kullanılır. Örneğin: insan yaşı bilgisini "int" veri tipinde tutmak hafızada fazladan alan kaplamak demek olacaktır. Zaten insan yaşı "int" değerinden çok küçüktür. Bunun için "byte" tipinde bir değişken tanımlamak hafızayı etkin kullanmayı sağlayacaktır.

Örnek Tanımlama:

```java
int i1 = 2147483647;
int i2 = -2147483648;
```

#### "long" Veri Tipi

64 Bit'lik (yani 8 Byte) veri büyüklüğüne sahip tam sayı değeridir. Tam sayı veri tipleri içinde en büyük değer aralığına sahip veri tipidir. Çok büyük basamaklı sayıları tutabilmek için idealdir. Long tipindeki değişkenlere atanan verilerin sonunda "L" son eki vardır. Hafızada önemli bir yer kaplar. Kullanırken dikkatli olmak gerekir.

-9,223,372,036,854,775,808 ile 9,223,372,036,854,775,807 arasında değer alabilir.

Örnek Tanımlama:

```java
long l1 = 9223372036854775807L;
long l2 = -9223372036854775808L;
```

#### "float" Veri Tipi

32 Bit'lik (yani 4 Byte) veri büyüklüğüne sahip ondalıklı sayı değeridir. Sayı aralığına bir limit getirilmemiştir. Hafızayı etkin kullanmak adına "double" veri tipi yerine tercih edilebilir. Çünkü, "double" veri tipi "float" 'dan daha büyük bir yer kaplamaktadır. Varsayılan değeri 0.0F şeklindedir. Float tipindeki değişkenlere atanan verilerin sonunda "f" son eki vardır. Değişkene atanan değerin "float" tipinde olduğunu belirtir. Tavsiye olarak da bu veri türü asla para birimi gibi kesin bir değerler için kullanılmamalıdr.

Örnek Tanımlama:

```java
float f1 = 3.14f;
float f2 = 3.14F;
```

#### "double" Veri Tipi

64 Bit'lik (yani 8 Byte) veri büyüklüğüne sahip ondalıklı sayı değeridir. Sayı aralığına bir limit getirilmemiştir. Boyutu büyük olduğu için tanımlama yapılırken gerçekten "float" veri tipinin yetersiz olduğu durumlarda kullanılmalıdır. Varsayılan değeri 0.0d şeklindedir. Atanan verinin sonuna "d" son eki koyularak "double" tipte bir veri olduğu belirtilebilir. Fakat, "d" son ekinin koyulmadığı durumlarda ondalıklı sayı verisi varsayılan olarak "double" olarak kabul edilir. Konulması zorunlu değildir.

Örnek Tanımlama:

```java
double d1 = 3.14;
double d2 = 3.14d;
```

#### "char" Veri Tipi

16 Bit'lik (yani 2 Byte) büyüklüğüne sahip karakter verilerini tutar. Unicode tipinde karakter verilerini saklar. '\u0000' (0) ile '\uffff' (65535) aralığında değer alır.

Örnek Tanımlama:

```java
char c1 = 'a';
char c2 = 'A';
```