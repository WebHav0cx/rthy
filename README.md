# rthy

<button
                key={tab}
                onClick={() => setActiveTab(tab)}
                className={`px-4 py-2 border-x border-t rounded text-sm md:text-base hover:border ${
                  activeTab === tab
                    ? "bg-white text-black font-bold"
                    : "bg-white text-red-600"
                }hover:bg-gray-200`}
              >
                {tab}
              </button>
