// README FIRST 
// Ye React + Tailwind based Music/Artist website hai
// Modern, dark, animated — option 2 + 5 full badass combo

// ===============================
// FILE: src/App.jsx
// ===============================

import { motion } from "framer-motion";
import { Play, Music, Instagram, Youtube } from "lucide-react";

export default function App() {
  return (
    <div className="min-h-screen bg-gradient-to-br from-black via-slate-900 to-black text-white">

      {/* HERO SECTION */}
      <section className="flex flex-col items-center justify-center text-center px-6 py-32">
        <motion.h1
          initial={{ opacity: 0, y: 40 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.8 }}
          className="text-5xl md:text-7xl font-bold mb-6"
        >
          YOUR ARTIST NAME
        </motion.h1>

        <motion.p
          initial={{ opacity: 0, y: 20 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ delay: 0.3 }}
          className="text-gray-400 max-w-xl"
        >
          Independent artist. Real music. No filters.
        </motion.p>

        <motion.button
          whileHover={{ scale: 1.1 }}
          className="mt-10 flex items-center gap-3 bg-white text-black px-8 py-3 rounded-full font-semibold"
        >
          <Play size={18} /> Listen Now
        </motion.button>
      </section>

      {/* TRACKS */}
      <section className="max-w-6xl mx-auto px-6 py-24 grid md:grid-cols-3 gap-6">
        {["Track One", "Track Two", "Track Three"].map((track, i) => (
          <motion.div
            key={i}
            whileHover={{ y: -10 }}
            className="bg-slate-800/60 backdrop-blur p-6 rounded-2xl shadow-xl"
          >
            <Music className="mb-4 text-indigo-400" />
            <h3 className="text-xl font-semibold">{track}</h3>
            <p className="text-gray-400 text-sm mt-2">Genre • Year</p>
          </motion.div>
        ))}
      </section>

      {/* SOCIALS */}
      <footer className="py-16 flex justify-center gap-8 text-gray-400">
        <a href="#"><Instagram /></a>
        <a href="#"><Youtube /></a>
      </footer>

    </div>
  );
}

// ===============================
// STACK USED:
// React + Tailwind CSS
// Framer Motion (animations)
// Lucide Icons
// ===============================
