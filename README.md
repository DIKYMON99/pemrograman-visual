# pemrograman-visual
using System;

class TebakAngka
{
    static void Main()
    {
        Random random = new Random();
        int angkaRahasia = random.Next(1, 101); // Angka acak antara 1-100
        int tebakan = 0;
        int jumlahPercobaan = 0;

        Console.WriteLine("Selamat datang di Game Tebak Angka!");
        Console.WriteLine("Saya sudah memilih angka antara 1 hingga 100. Coba tebak!");

        while (tebakan != angkaRahasia)
        {
            Console.Write("Masukkan tebakan Anda: ");
            string input = Console.ReadLine();

            if (int.TryParse(input, out tebakan))
            {
                jumlahPercobaan++;
                
                if (tebakan < angkaRahasia)
                {
                    Console.WriteLine("Terlalu kecil! Coba lagi.");
                }
                else if (tebakan > angkaRahasia)
                {
                    Console.WriteLine("Terlalu besar! Coba lagi.");
                }
                else
                {
                    Console.WriteLine($"Selamat! Anda menebak angka {angkaRahasia} dengan {jumlahPercobaan} percobaan.");
                }
            }
            else
            {
                Console.WriteLine("Masukkan angka yang valid!");
            }
        }

        Console.WriteLine("Terima kasih telah bermain!");
    }
}

\\\\\
