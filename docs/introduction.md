import React from "react"; import { Button } from "@/components/ui/button"; import { Card, CardContent } from "@/components/ui/card"; import { Input } from "@/components/ui/input"; import { Progress } from "@/components/ui/progress"; import { Volume2, Star } from "lucide-react";

export default function ReadingApp() { return ( <div className="min-h-screen bg-yellow-100 p-4 flex flex-col items-center"> <h1 className="text-3xl font-bold mb-4 text-center text-orange-700"> Avşin ile Okuma Zamanı </h1>

<Card className="w-full max-w-md bg-white shadow-xl rounded-2xl p-4">
    <CardContent className="flex flex-col items-center space-y-4">
      <div className="text-4xl font-bold text-orange-500">A</div>

      <Button className="flex items-center space-x-2 bg-orange-300 hover:bg-orange-400">
        <Volume2 className="w-5 h-5" />
        <span>Harfi Dinle</span>
      </Button>

      <div className="w-full">
        <label className="block text-sm font-medium mb-1">Parmağınla A harfini çiz:</label>
        <div className="h-40 bg-orange-100 rounded-xl border border-orange-300 flex items-center justify-center">
          <span className="text-orange-400">(Çizim Alanı)</span>
        </div>
      </div>

      <div className="text-lg font-semibold text-gray-700">
        A ile başlayan kelime: <span className="text-orange-600">Arı</span>
      </div>

      <img
        src="/images/ari.png"
        alt="Arı"
        className="w-32 h-32 object-contain"
      />

      <Progress value={25} className="w-full" />
      <div className="text-sm text-gray-500">1 / 26 Harf Tamamlandı</div>
    </CardContent>
  </Card>

  <div className="flex space-x-4 mt-6">
    <Button variant="outline">Geri</Button>
    <Button className="bg-orange-500 hover:bg-orange-600 text-white">İleri</Button>
  </div>

  <div className="mt-8 text-yellow-800 flex items-center space-x-2">
    <Star className="w-5 h-5" />
    <span>Bugün 3 harf öğrendin, harikasın!</span>
  </div>
</div>

); }

