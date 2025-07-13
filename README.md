import { useEffect } from "react";
import { motion } from "framer-motion";

export default function WeddingInvitation() {
  useEffect(() => {
    document.title = "The Wedding of Aldi & Sinta";
  }, []);

  return (
    <div className="bg-[#fdf9f6] text-[#5a4d40] font-serif">
      {/* Cover Section */}
      <section className="h-screen flex flex-col justify-center items-center text-center bg-[url('/cover-image.jpg')] bg-cover bg-center">
        <motion.div
          initial={{ opacity: 0 }}
          animate={{ opacity: 1 }}
          transition={{ duration: 1.2 }}
          className="bg-white bg-opacity-80 p-6 rounded-2xl shadow-xl"
        >
          <h1 className="text-3xl md:text-5xl font-bold mb-2">Aldi & Sinta</h1>
          <p className="text-md md:text-lg">Kepada Yth. Bapak/Ibu/Saudara/i</p>
          <p className="italic mt-1">Kami mengundang Anda untuk hadir di hari bahagia kami</p>
        </motion.div>
      </section>

      {/* Couple Section */}
      <section className="py-16 px-6 text-center bg-white">
        <h2 className="text-2xl md:text-3xl font-semibold mb-8">Bride & Groom</h2>
        <div className="flex flex-col md:flex-row justify-center items-center gap-10">
          <div>
            <img src="/sinta.jpg" alt="Sinta" className="w-40 h-40 rounded-full mx-auto shadow-lg" />
            <p className="mt-4 font-bold text-xl">Sinta Ayu</p>
            <p className="text-sm">Putri dari Bapak Surya & Ibu Ningsih</p>
          </div>
          <span className="text-4xl">&</span>
          <div>
            <img src="/aldi.jpg" alt="Aldi" className="w-40 h-40 rounded-full mx-auto shadow-lg" />
            <p className="mt-4 font-bold text-xl">Aldi Pratama</p>
            <p className="text-sm">Putra dari Bapak Joko & Ibu Dewi</p>
          </div>
        </div>
      </section>

      {/* Event Details */}
      <section className="py-16 px-6 text-center bg-[#fffaf6]">
        <h2 className="text-2xl md:text-3xl font-semibold mb-8">Akad & Resepsi</h2>
        <div className="space-y-6">
          <div>
            <h3 className="font-bold text-xl">Akad Nikah</h3>
            <p>Minggu, 17 Agustus 2025</p>
            <p>Pukul 09.00 WIB</p>
            <p>Gedung Nusantara, Yogyakarta</p>
          </div>
          <div>
            <h3 className="font-bold text-xl">Resepsi</h3>
            <p>Minggu, 17 Agustus 2025</p>
            <p>Pukul 11.00 - 14.00 WIB</p>
            <p>Gedung Nusantara, Yogyakarta</p>
          </div>
        </div>
      </section>

      {/* Gallery Section */}
      <section className="py-16 px-6 bg-white">
        <h2 className="text-center text-2xl md:text-3xl font-semibold mb-8">Galeri Cinta Kami</h2>
        <div className="grid grid-cols-2 md:grid-cols-3 gap-4">
          {[1, 2, 3, 4, 5, 6].map((i) => (
            <img
              key={i}
              src={`/gallery-${i}.jpg`}
              alt={`gallery-${i}`}
              className="w-full h-60 object-cover rounded-xl shadow"
            />
          ))}
        </div>
      </section>

      {/* RSVP Section */}
      <section className="py-16 px-6 text-center bg-[#fef6ef]">
        <h2 className="text-2xl md:text-3xl font-semibold mb-6">Konfirmasi Kehadiran</h2>
        <p className="mb-4">Silakan isi formulir konfirmasi kehadiran Anda</p>
        <form className="max-w-md mx-auto space-y-4">
          <input
            type="text"
            placeholder="Nama Anda"
            className="w-full px-4 py-2 border rounded"
          />
          <select className="w-full px-4 py-2 border rounded">
            <option>Hadir</option>
            <option>Tidak Hadir</option>
          </select>
          <button type="submit" className="bg-[#a07f68] text-white px-6 py-2 rounded shadow">
            Kirim
          </button>
        </form>
      </section>

      {/* Footer */}
      <footer className="text-center text-sm py-6 bg-white text-gray-500">
        &copy; 2025 Aldi & Sinta Wedding Invitation
      </footer>
    </div>
  );
}
