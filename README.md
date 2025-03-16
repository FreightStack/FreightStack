import React from "react";
import Head from "next/head";

export default function HeavyHaulCargo() {
  const services = [
    { img: "/icons/data-center.svg", title: "Data Centers", desc: "Expert handling and transport of hyperscale and colocation data center equipment." },
    { img: "/icons/energy.svg", title: "Energy Sector", desc: "Safe and efficient transport of energy infrastructure components." },
    { img: "/icons/oil-gas.svg", title: "Oil & Gas", desc: "Heavy haul services for oil rigs, pipelines, and refinery equipment." },
    { img: "/icons/infrastructure.svg", title: "Infrastructure", desc: "Specialized transportation for large-scale construction projects." },
  ];

  console.log("Services Data:", services);

  return (
    <>
      <Head>
        <title>Freight Stack - Heavy Haul Specialized Cargo</title>
        <meta name="description" content="Expert transportation for Data Centers, Energy, Oil & Gas, and Infrastructure." />
        <meta name="viewport" content="width=device-width, initial-scale=1" />
      </Head>
      <div className="min-h-screen bg-gray-100 p-6">
        {/* Hero Section */}
        <div 
          className="relative bg-cover bg-center h-96 flex items-center justify-center text-white text-center px-6"
          style={{ backgroundImage: "url('/images/hero-bg.jpg')", backgroundSize: 'cover', backgroundPosition: 'center' }}
        >
          <div className="bg-black bg-opacity-60 p-8 rounded-lg shadow-lg">
            <h1 className="text-5xl font-bold">Reliable Heavy Haul Solutions</h1>
            <p className="text-lg mt-2 max-w-lg mx-auto">We specialize in energy, oil & gas, and infrastructure transport.</p>
            <a href="#quote" className="mt-4 inline-block px-8 py-3 text-lg bg-yellow-500 hover:bg-yellow-600 transition text-white rounded-md shadow-md">Get a Free Quote</a>
          </div>
        </div>

        {/* Services Section */}
        <section className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 mt-16 px-6">
          {services && services.length > 0 ? (
            services.map((service, index) => (
              <div key={index} className="bg-white p-8 shadow-lg rounded-xl text-center hover:shadow-2xl transition duration-300 transform hover:-translate-y-2">
                <img 
                  src={service.img || "/icons/default.svg"} 
                  alt={service.title} 
                  className="w-16 h-16 mx-auto mb-6" 
                  onError={(e) => { e.target.src = "/icons/default.svg"; }}
                />
                <h2 className="text-2xl font-semibold">{service.title}</h2>
                <p className="text-gray-600 mt-3">{service.desc}</p>
              </div>
            ))
          ) : (
            <p className="text-center text-gray-600 text-lg">No services available at the moment.</p>
          )}
        </section>
      </div>
    </>
  );
}
