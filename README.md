# Algorithm Exercises With C#

C# dilini öğrenirken karşılaştığım algoritma sorularını çözümleriyle birlikte bu repoda bir araya getirdim.

- Kullanıcıdan alınan iki sayının toplamını ekrana yazdıran program
    
    ```csharp
    Console.Write("Birinci sayıyı gir: ");
    int s1 = Convert.ToInt32(Console.ReadLine());
    Console.Write("İkinci sayıyı gir: ");
    int s2 = Convert.ToInt32(Console.ReadLine());
    
    int sum = s1+ s2;
    
    Console.WriteLine(sum);
    ```
    
- Bir sayının karesini metot kullanmadan hesaplayıp ekrana yazdıran program
    
    ```csharp
    Console.Write("Tabanı girin: ");
    int s1 = Convert.ToInt32(Console.ReadLine());
    Console.Write("Üssü gir: ");
    int s2 = Convert.ToInt32(Console.ReadLine());
    
    int pow = 1;
    
    for (int i = s2; i > 0; i--)
    {
    	pow = pow * s1;
    }
    Console.WriteLine(pow);
    ```
    
- Kullanıcıdan alınan iki sayının ortalamasını hesaplayıp ekrana yazdıran program
    
    ```csharp
    Console.Write("İlk sayıyı gir: ");
    int s1 = Convert.ToInt32(Console.ReadLine());
    Console.Write("İkinci sayıyı gir: ");
    int s2 = Convert.ToInt32(Console.ReadLine());
    
    int ort = (s1 + s2)/2;
    Console.WriteLine(ort);
    ```
    
- Yarı çap uzunluğunun kullanıcıdan alındığı bir dairenin alanını ve çevresini hesaplayıp ekrana yazdıran program
    
    ```csharp
    Console.Write("Yarı çap uzunluğunu gir: ");
    double r = Convert.ToInt32(Console.ReadLine());
    double pi = 3.14;
    double cevre = 2 * pi * r;
    double alan = pi * r * r;
    Console.WriteLine("Çevre: " + cevre + " birim");
    Console.WriteLine("Alan: " + alan + " birim kare");
    ```
    
- Kullanıcıdan alınan Fahrenheit'ı Celsius'a çevirip ekrana yazdıran program
    
    ```csharp
    Console.Write("Fahrenheit değerini girin: ");
    double fhrn = Convert.ToDouble(Console.ReadLine());
    double cels = (fhrn - 32) / 1.8000;
    Console.WriteLine("Celsius: " + cels);
    ```
    
- Bir sayının pozitif, negatif veya sıfır olduğunu kontrol eden program
    
    ```csharp
    Console.Write("Sayı gir: ");
    int s1 = Convert.ToInt32(Console.ReadLine());
    if (s1 > 0) Console.WriteLine("Sayı pozitif");	
    else if (s1 < 0) Console.WriteLine("Sayı negatif");
    else Console.WriteLine("Sayı sıfır");
    ```
    
- Kullanıcının girdiği üç sayıdan en büyüğünü metot kullanmadan bulup ekrana yazdıran programı
    
    ```csharp
    Console.Write("İlk sayıyı gir: ");
    int s1 = Convert.ToInt32(Console.ReadLine());Console.Write("İkinci sayıyı gir: ");
    int s2 = Convert.ToInt32(Console.ReadLine());
    Console.Write("Üçüncü sayıyı gir: ");
    int s3 = Convert.ToInt32(Console.ReadLine());
    
    int enb = s1;
    if (s2 > enb) enb = s2;
    if (s3 > enb) enb = s3;
    
    Console.WriteLine(enb);
    ```
    
- Kullanıcın girdiği bir sayının tek mi çift mi olduğunu kontrol eden program
    
    ```csharp
    Console.Write("Sayıyı gir: ");
    int s1 = Convert.ToInt32(Console.ReadLine());
    
    if (s1 % 2 == 0) Console.WriteLine("Sayı çift");
    else Console.WriteLine("Sayı tek");
    ```
    
- 1'den 10'a kadar olan sayıları ekrana alt alta yazdıran bir program
    
    ```csharp
    for (int i = 1; i <= 10; i++)
    {
      Console.WriteLine(i);
    }
    ```
    
- Kullanıcı tarafından girilen sayının faktöriyelini hesaplayan program
    
    ```csharp
    Console.Write("Sayı gir: ");
    int s1 = Convert.ToInt32(Console.ReadLine());
    int fakt = 1;
    
    for (int i = 1; i <= s1; i++)
    {
    	fakt = fakt * i;
    }
    Console.WriteLine(fakt);
    ```
    
- 1!+2!+3!+4!...+n! şeklinde devam eden faktöriyeller toplamından n sayısı kullanıcı tarafından girildiğinde işlemin sonucunu bulan program
    
    ```csharp
    Console.Write("N sayısını girin: ");
    int n = Convert.ToInt32(Console.ReadLine());
    
    int tpl = 0;
    for (int i = 1; i <= n; i++)
    {
      int fakt = 1;
      for (int j = i; j > 1; j--)
      {
        fakt = fakt * j;
      }
        tpl = tpl + fakt;
    }
    Console.WriteLine("Girilen N sayısına kadar olan sayıların faktoriyellerinin toplamı: " + tpl);
    ```
    
- Fibonacci serisinin ilk 10 terimini hesaplayıp ekrana yazdıran program
    
    ```csharp
    int n1 = 0, n2 = 1, n3;
    int count = 10;
    Console.Write(n1 + " " + n2 + " ");
    
    for (int i = 2; i < count; i++)
    {
    	n3 = n1 + n2;
    	Console.Write(n3 + " ");
    	n1 = n2;
    	n2 = n3;
    }
    ```
    
- Bir sayının asal olup olmadığını kontrol eden program
    
    ```csharp
    Console.Write("Bir sayı gir: ");
    int sayi = Convert.ToInt32(Console.ReadLine());
    
    bool asal = true;
    
    if (sayi <= 1) asal = false;
    
    else
    {
    	for (int i = 2; i <= Math.Sqrt(sayi); i++)
    	{
    		if (sayi % i == 0)
    		{
    			asal = false;
    			break;
    		}
    	}
    }
    
    if (asal) Console.WriteLine(sayi + " bir asal sayıdır.");
    else Console.WriteLine(sayi + " bir asal sayı değildir.");
    ```
    
- Kullanıcı tarafından girilen iki sayının EBOB ve EKOK'unu bulma
    
    ```csharp
    int s1 = Convert.ToInt32(Console.ReadLine());
    int s2 = Convert.ToInt32(Console.ReadLine());
    
    int a = s1;
    int b = s2;
    int EBOB = 0;
    
    while (b != 0)
    {
    	int temp = b;
    	b = a % b;
    	a = temp;
    }
    
    EBOB = a;
    
    int EKOK = (s1 * s2) / EBOB;
    
    Console.WriteLine("EBOB = " + EBOB);
    Console.WriteLine("EKOK = " + EKOK);
    ```
    
- Öğrenci sayısı kullanıcı tarafından girilen bir sınıfta; öğrenci yaşları kullanıcı tarafından girilsin, sınıftaki en küçük yaşı, en büyük yaşı, sınıfın yaş ortalamasını ve sınıfta kaç kişinin 20 yaşında olduğunu bulan program
    
    ```csharp
    Console.Write("Öğrenci sayısı gir: ");
    int ogrsay = Convert.ToInt32(Console.ReadLine());
    
    int ekck = 0;
    int ebyk = 0;
    int tpl = 0;
    int yirmisayac = 0;
    
    for (int i = 0; i < ogrsay; i++)
    {
    	Console.Write("{0}. öğrencinin yaşını gir: ", i + 1);
    	int yas = Convert.ToInt32(Console.ReadLine());
    	tpl += yas;
    	if (ekck == 0) ekck = yas;
    	if (yas < ekck) ekck = yas;
    	if (yas > ebyk) ebyk = yas;
    	if (yas == 20) yirmisayac++;
    }
    int ort = tpl / ogrsay;
    
    Console.WriteLine("En küçük yaş: " + ekck);
    Console.WriteLine("En büyük yaş: " + ebyk);
    Console.WriteLine("Ortalama yaş: " + ort);
    Console.WriteLine("20 yaş sayısı: " + yirmisayac);
    ```
    
- Bir dizideki elemanların toplamını hesaplayıp ekrana yazdıran program
    
    ```csharp
    		int[] dizi = new int[] { 1, 2, 3, 4, 5 };
    		int tpl = 0;
    		for (int i = 0; i < dizi.Length; i++)
    		{
    			tpl = tpl + dizi[i];
    		}
    		Console.WriteLine(tpl);
    ```
    
- Boyutu kullanıcı tarafından belirlenen diziyi bilgisayar tarafından rastgele tutulan sayılardan çift olanlarıyla sondan başlayarak dolduran program
    
    ```csharp
    Console.Write("Dizinin boyutunu gir: ");
    int gs = Convert.ToInt32(Console.ReadLine());
    Random random = new Random();
    int[] dizi = new int[gs];
    int ts = 0;
    
    for (int i = gs - 1; i >= 0; i--)
    {
    	ts = random.Next(0, 100);
    	if (ts % 2 == 0)
    	{
    		dizi[i] = ts;
    	}
    		else i++;
    }
    
    foreach (int i in dizi)
    {
    	Console.Write(" " + i);
    }
    ```
