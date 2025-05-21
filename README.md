import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
import { Textarea } from "@/components/ui/textarea";
import { BadgeCheck, ShoppingCart, ShieldCheck } from "lucide-react";

export default function EcoPiMarket() {
  return (
    <div className="p-6 max-w-5xl mx-auto space-y-6">
      <h1 className="text-3xl font-bold text-center">Eco Pi Market (Beta)</h1>
      <p className="text-center text-sm text-gray-500">
        Platform jual beli berasaskan Pi yang patuh syariah dan dipacu komuniti.
      </p>

      <Card>
        <CardContent className="space-y-4 p-4">
          <h2 className="text-xl font-semibold flex items-center gap-2">
            <ShoppingCart size={20} /> Iklan Produk
          </h2>
          <Input placeholder="Nama Produk" />
          <Input placeholder="Harga (dalam Pi)" />
          <Input placeholder="Lokasi Penghantaran" />
          <Textarea placeholder="Penerangan produk, kaedah penghantaran, syarat akad dll" />
          <Input placeholder="Wallet Pi Penjual" />
          <Button className="w-full">Hantar Iklan</Button>
        </CardContent>
      </Card>

      <Card>
        <CardContent className="space-y-4 p-4">
          <h2 className="text-xl font-semibold flex items-center gap-2">
            <ShieldCheck size={20} /> Tips Urus Niaga Selamat
          </h2>
          <ul className="list-disc pl-5 text-sm text-gray-700 space-y-1">
            <li>Utamakan transaksi COD (Cash on Delivery)</li>
            <li>Jika perlu penghantaran, minta bukti pos & bayar separuh dahulu</li>
            <li>Gunakan akad digital: "Saya jual...", "Saya beli..."</li>
            <li>Lapor ahli mencurigakan kepada admin</li>
          </ul>
        </CardContent>
      </Card>

      <Card>
        <CardContent className="space-y-4 p-4">
          <h2 className="text-xl font-semibold flex items-center gap-2">
            <BadgeCheck size={20} /> Komuniti Amanah
          </h2>
          <p className="text-sm text-gray-700">
            Ahli yang telah melengkapkan 5 transaksi berjaya boleh mohon status "Trusted Seller" untuk membina keyakinan pembeli.
          </p>
          <Button variant="outline">Mohon Trusted Seller</Button>
        </CardContent>
      </Card>
    </div>
  );
}


