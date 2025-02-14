import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { MapPin, Mail, Phone } from "lucide-react";
import { motion } from "framer-motion";

const HomePage = () => {
  return (
    <div className="min-h-screen bg-gray-100">
      {/* Fondo con temática de construcción */}
      <div
        className="bg-cover bg-center h-[300px] flex items-center justify-center"
        style={{ backgroundImage: "url('/construction-bg.jpg')" }}
      >
        <h1 className="text-white text-5xl font-bold text-center shadow-lg p-4 bg-black/50 rounded-xl">
          EGJ SERVICES GROUP
        </h1>
      </div>

      {/* Sección de Información */}
      <div className="container mx-auto px-6 lg:px-16 py-12 grid grid-cols-1 lg:grid-cols-2 gap-12">
        <motion.div
          initial={{ opacity: 0, x: -50 }}
          animate={{ opacity: 1, x: 0 }}
          className="text-lg text-gray-800"
        >
          <p className="mb-4">
            EGJ Services Group specializes in three-axle truck transportation, hauling
            aggregates and excess materials across Palm Beach, St. Lucie, and Broward Counties.
          </p>
          <p className="mb-4">
            We ensure fast deliveries, exceptional service, transparency, and competitive pricing.
            Trust us for efficient and reliable hauling solutions that keep your projects on track!
          </p>
          <Button className="mt-4">Get a Quote</Button>
        </motion.div>

        {/* Imágenes relacionadas con construcción */}
        <motion.div
          initial={{ opacity: 0, x: 50 }}
          animate={{ opacity: 1, x: 0 }}
          className="grid grid-cols-2 gap-4"
        >
          <img src="/truck.jpg" alt="Truck" className="rounded-lg shadow-lg w-full h-40 object-cover" />
          <img src="/construction-site.jpg" alt="Construction Site" className="rounded-lg shadow-lg w-full h-40 object-cover" />
          <img src="/materials.jpg" alt="Materials" className="rounded-lg shadow-lg w-full h-40 object-cover" />
          <img src="/asphalt.jpg" alt="Asphalt" className="rounded-lg shadow-lg w-full h-40 object-cover" />
        </motion.div>
      </div>

      {/* Mapa con ubicación */}
      <div className="container mx-auto px-6 lg:px-16 py-12">
        <h2 className="text-3xl font-bold text-center mb-6">Find Us</h2>
        <iframe
          title="EGJ Location"
          className="w-full h-[400px] rounded-lg shadow-lg"
          src="https://www.google.com/maps/embed/v1/place?key=YOUR_GOOGLE_MAPS_API_KEY&q=PO+BOX+17017,West+Palm+Beach,FL+33416"
          allowFullScreen
        ></iframe>
      </div>

      {/* Contacto */}
      <div className="bg-gray-800 text-white py-12">
        <div className="container mx-auto px-6 lg:px-16 grid grid-cols-1 md:grid-cols-3 gap-8 text-center">
          <div className="flex flex-col items-center">
            <MapPin className="w-10 h-10 mb-2" />
            <p>PO BOX 17017, West Palm Beach, FL 33416</p>
          </div>
          <div className="flex flex-col items-center">
            <Mail className="w-10 h-10 mb-2" />
            <p>egjttrucking@gmail.com</p>
          </div>
          <div className="flex flex-col items-center">
            <Phone className="w-10 h-10 mb-2" />
            <p>561-506-8932</p>
          </div>
        </div>
      </div>
    </div>
  );
};

export default HomePage;
