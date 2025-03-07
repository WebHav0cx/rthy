<button
  key={tab}
  onClick={() => setActiveTab(tab)}
  className={`px-4 py-2 border-x border-t rounded text-sm md:text-base hover:border 
    ${activeTab === tab ? "bg-white text-black font-bold" : "bg-white text-green-500"} 
    hover:bg-gray-200`}
>
  {tab}
</button>


https://documenter.getpostman.com/view/24316849/2sAYX2M43f


import React, { useState } from "react";
import { Link } from "react-router-dom";
import { Icon } from "@iconify/react";

function Navbar() {
  const [isMenuOpen, setIsMenuOpen] = useState(false);

  console.log("Navbar is rendering!"); // Debugging Log

  return (
    <div className="w-screen mx-auto px-8 py-4 bg-green-500">
      <nav className="flex justify-around items-center">
        <Link to="/" className="text-white font-bold">Verify Hub</Link>
        <button
          className="text-white text-2xl md:hidden"
          onClick={() => setIsMenuOpen(!isMenuOpen)}
          aria-label="Toggle Menu"
        >
          <Icon icon="mingcute:menu-fill" width="24" height="24" />
        </button>
        <div className={`md:flex ${isMenuOpen ? "block" : "hidden"}`}>
          <ul className="flex flex-col md:flex-row gap-4">
            <li><Link to="/" className="text-white">Home</Link></li>
            <li><Link to="/about" className="text-white">About</Link></li>
            <li><Link to="/services" className="text-white">Services</Link></li>
            <li><Link to="/contact" className="text-white">Contact</Link></li>
          </ul>
        </div>
      </nav>
    </div>
  );
}

export default Navbar;
