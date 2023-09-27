/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 */
package com.mycompany.praktikum3;

import java.util.Scanner;

/**
 *
 * @author Lenovo
 */
public class Praktikum3 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        
        int jumlahPembelian = 0;
        int menit = 0;
        int stoksisa = 150;
        int hasilpembelian = 0;
        int hargaSemangka = 100000;

        System.out.println("===== TOKO BUAH A =====");
        System.out.print("Enter jumlah pembelian : ");
        jumlahPembelian = input.nextInt();

        if (jumlahPembelian <= 0 || jumlahPembelian > stoksisa) {
            System.err.println("ERROR - Masukkan jumlah pembelian yang valid!");
        } else {
            System.out.print("Enter menit : ");
            menit = input.nextInt();

            if (menit <= 0) {
                System.err.println("ERROR - Masukkan nputan tidak valid!");
            } else if (menit > 420) {
                System.err.println("Toko Tutup!");
            } else {
                int potongan = (menit / 40) * 5;

                hasilpembelian = jumlahPembelian * hargaSemangka;
                int totalPotongan = (hasilpembelian * potongan) / 100;
                hasilpembelian -= totalPotongan;

                stoksisa -= jumlahPembelian;

                System.out.println("===============================");
                System.out.println("Jumlah Pembelian : " + jumlahPembelian);
                System.out.println("Stok Tersisa : " + stoksisa);
                System.out.println("Hasil Pembelian : Rp" + hasilpembelian);

            }
        }
    }
}


