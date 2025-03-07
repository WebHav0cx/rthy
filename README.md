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