
<!---
FreightStack/FreightStack is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->import React from "react";
import Head from "next/head";

export default function HeavyHaulCargo() {
  return (
    <>
      <Head>
        <title>Freight Stack - Heavy Haul Specialized Cargo</title>
        <meta name="description" content="Expert transportation for Data Centers, Energy, Oil & Gas, and Infrastructure." />
      </Head>
      <div className="min-h-screen bg-gray-100 p-6">
        {/* Hero Section */}
        <div className="relative bg-cover bg-center h-96 flex items-center justify-center text-white text-center" style={{ backgroundImage: "url('/images/hero-bg.jpg')" }}>
          <div className="bg-black bg-opacity-50 p-6 rounded-lg">
            <h1 className="text-4xl font-bold">Heavy Haul Specialized Cargo</h1>
            <p className="text-lg mt-2">Reliable transportation for critical industries</p>
            <a href="#quote" className="mt-4 inline-block px-6 py-2 text-lg bg-blue-500 hover:bg-blue-600 transition text-white rounded-md">Request a Quote</a>
          </div>
        </div>

        {/* Services Section */}
        <section className="grid grid-cols-1 md:grid-cols-4 gap-6 mt-12 px-4 md:px-12">
          {[
            { img: "/icons/data-center.svg", title: "Data Centers", desc: "Expert handling and transport of hyperscale and colocation data center equipment." },
            { img: "/icons/energy.svg", title: "Energy Sector", desc: "Safe and efficient transport of energy infrastructure components." },
            { img: "/icons/oil-gas.svg", title: "Oil & Gas", desc: "Heavy haul services for oil rigs, pipelines, and refinery equipment." },
            { img: "/icons/infrastructure.svg", title: "Infrastructure", desc: "Specialized transportation for large-scale construction projects." },
          ].map((service, index) => (
            <div key={index} className="bg-white p-6 shadow-lg rounded-lg text-center hover:shadow-2xl transition">
              <img src={service.img} alt={service.title} className="w-14 h-14 mx-auto mb-4" />
              <h2 className="text-xl font-semibold">{service.title}</h2>
              <p className="text-gray-600">{service.desc}</p>
            </div>
          ))}
        </section>
      </div>
    </>
  );
}

