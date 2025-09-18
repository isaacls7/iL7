import { useState } from "react";

export default function RecargaPage() {
  const [playerId, setPlayerId] = useState("");
  const [selected, setSelected] = useState(null);
  const [success, setSuccess] = useState(false);

  const opcoes = [
    { preco: 6, pontos: "60 点券" },
    { preco: 10, pontos: "100 点券" },
    { preco: 30, pontos: "300 + 8 点券" },
    { preco: 68, pontos: "680 + 20 点券" },
    { preco: 128, pontos: "1280 + 38 点券" },
    { preco: 198, pontos: "3280 + 28 点券" },
    { preco: 648, pontos: "6480 + 73 点券" },
  ];

  const handleCompra = () => {
    if (playerId && selected !== null) {
      setSuccess(true);
    }
  };

  return (
    <div className="min-h-screen bg-gradient-to-r from-purple-900 to-indigo-900 flex flex-col items-center justify-center p-6">
      {!success ? (
        <div className="w-full max-w-md p-6 bg-black/40 text-white rounded-xl shadow-lg">
          <h1 className="text-2xl font-bold mb-4 text-center">购买点券</h1>
          <input
            placeholder="请输入玩家ID"
            value={playerId}
            onChange={(e) => setPlayerId(e.target.value)}
            className="mb-4 w-full p-2 rounded bg-black/30 border border-gray-600 text-white"
          />
          <div className="space-y-3">
            {opcoes.map((op, idx) => (
              <div
                key={idx}
                className={`cursor-pointer transition p-3 rounded-xl ${
                  selected === idx ? "bg-indigo-600" : "bg-black/30"
                }`}
                onClick={() => setSelected(idx)}
              >
                <div className="flex justify-between items-center text-lg">
                  <span>{op.preco} 元</span>
                  <span>{op.pontos}</span>
                </div>
              </div>
            ))}
          </div>
          <button
            onClick={handleCompra}
            disabled={!playerId || selected === null}
            className="mt-6 w-full p-3 rounded-lg bg-green-600 hover:bg-green-700 disabled:opacity-50"
          >
            确认购买
          </button>
        </div>
      ) : (
        <div className="w-full max-w-md p-6 bg-black/40 text-white text-center rounded-xl shadow-lg">
          <h2 className="text-2xl font-bold mb-2">购买成功 ✅</h2>
          <p className="mb-2">ID: {playerId}</p>
          <p className="mb-4">收到 {opcoes[selected].pontos}</p>
          <button
            onClick={() => {
              setSuccess(false);
              setPlayerId("");
              setSelected(null);
            }}
            className="p-3 rounded-lg bg-indigo-600 hover:bg-indigo-700"
          >
            OK
          </button>
        </div>
      )}
    </div>
  );
}import { useState } from "react";

export default function RecargaPage() {
  const [playerId, setPlayerId] = useState("");
  const [selected, setSelected] = useState(null);
  const [success, setSuccess] = useState(false);

  const opcoes = [
    { preco: 6, pontos: "60 点券" },
    { preco: 10, pontos: "100 点券" },
    { preco: 30, pontos: "300 + 8 点券" },
    { preco: 68, pontos: "680 + 20 点券" },
    { preco: 128, pontos: "1280 + 38 点券" },
    { preco: 198, pontos: "3280 + 28 点券" },
    { preco: 648, pontos: "6480 + 73 点券" },
  ];

  const handleCompra = () => {
    if (playerId && selected !== null) {
      setSuccess(true);
    }
  };

  return (
    <div className="min-h-screen bg-gradient-to-r from-purple-900 to-indigo-900 flex flex-col items-center justify-center p-6">
      {!success ? (
        <div className="w-full max-w-md p-6 bg-black/40 text-white rounded-xl shadow-lg">
          <h1 className="text-2xl font-bold mb-4 text-center">购买点券</h1>
          <input
            placeholder="请输入玩家ID"
            value={playerId}
            onChange={(e) => setPlayerId(e.target.value)}
            className="mb-4 w-full p-2 rounded bg-black/30 border border-gray-600 text-white"
          />
          <div className="space-y-3">
            {opcoes.map((op, idx) => (
              <div
                key={idx}
                className={`cursor-pointer transition p-3 rounded-xl ${
                  selected === idx ? "bg-indigo-600" : "bg-black/30"
                }`}
                onClick={() => setSelected(idx)}
              >
                <div className="flex justify-between items-center text-lg">
                  <span>{op.preco} 元</span>
                  <span>{op.pontos}</span>
                </div>
              </div>
            ))}
          </div>
          <button
            onClick={handleCompra}
            disabled={!playerId || selected === null}
            className="mt-6 w-full p-3 rounded-lg bg-green-600 hover:bg-green-700 disabled:opacity-50"
          >
            确认购买
          </button>
        </div>
      ) : (
        <div className="w-full max-w-md p-6 bg-black/40 text-white text-center rounded-xl shadow-lg">
          <h2 className="text-2xl font-bold mb-2">购买成功 ✅</h2>
          <p className="mb-2">ID: {playerId}</p>
          <p className="mb-4">收到 {opcoes[selected].pontos}</p>
          <button
            onClick={() => {
              setSuccess(false);
              setPlayerId("");
              setSelected(null);
            }}
            className="p-3 rounded-lg bg-indigo-600 hover:bg-indigo-700"
          >
            OK
          </button>
        </div>
      )}
    </div>
  );
}import { useState } from "react";

export default function RecargaPage() {
  const [playerId, setPlayerId] = useState("");
  const [selected, setSelected] = useState(null);
  const [success, setSuccess] = useState(false);

  const opcoes = [
    { preco: 6, pontos: "60 点券" },
    { preco: 10, pontos: "100 点券" },
    { preco: 30, pontos: "300 + 8 点券" },
    { preco: 68, pontos: "680 + 20 点券" },
    { preco: 128, pontos: "1280 + 38 点券" },
    { preco: 198, pontos: "3280 + 28 点券" },
    { preco: 648, pontos: "6480 + 73 点券" },
  ];

  const handleCompra = () => {
    if (playerId && selected !== null) {
      setSuccess(true);
    }
  };

  return (
    <div className="min-h-screen bg-gradient-to-r from-purple-900 to-indigo-900 flex flex-col items-center justify-center p-6">
      {!success ? (
        <div className="w-full max-w-md p-6 bg-black/40 text-white rounded-xl shadow-lg">
          <h1 className="text-2xl font-bold mb-4 text-center">购买点券</h1>
          <input
            placeholder="请输入玩家ID"
            value={playerId}
            onChange={(e) => setPlayerId(e.target.value)}
            className="mb-4 w-full p-2 rounded bg-black/30 border border-gray-600 text-white"
          />
          <div className="space-y-3">
            {opcoes.map((op, idx) => (
              <div
                key={idx}
                className={`cursor-pointer transition p-3 rounded-xl ${
                  selected === idx ? "bg-indigo-600" : "bg-black/30"
                }`}
                onClick={() => setSelected(idx)}
              >
                <div className="flex justify-between items-center text-lg">
                  <span>{op.preco} 元</span>
                  <span>{op.pontos}</span>
                </div>
              </div>
            ))}
          </div>
          <button
            onClick={handleCompra}
            disabled={!playerId || selected === null}
            className="mt-6 w-full p-3 rounded-lg bg-green-600 hover:bg-green-700 disabled:opacity-50"
          >
            确认购买
          </button>
        </div>
      ) : (
        <div className="w-full max-w-md p-6 bg-black/40 text-white text-center rounded-xl shadow-lg">
          <h2 className="text-2xl font-bold mb-2">购买成功 ✅</h2>
          <p className="mb-2">ID: {playerId}</p>
          <p className="mb-4">收到 {opcoes[selected].pontos}</p>
          <button
            onClick={() => {
              setSuccess(false);
              setPlayerId("");
              setSelected(null);
            }}
            className="p-3 rounded-lg bg-indigo-600 hover:bg-indigo-700"
          >
            OK
          </button>
        </div>
      )}
    </div>
  );
}import { useState } from "react";

export default function RecargaPage() {
  const [playerId, setPlayerId] = useState("");
  const [selected, setSelected] = useState(null);
  const [success, setSuccess] = useState(false);

  const opcoes = [
    { preco: 6, pontos: "60 点券" },
    { preco: 10, pontos: "100 点券" },
    { preco: 30, pontos: "300 + 8 点券" },
    { preco: 68, pontos: "680 + 20 点券" },
    { preco: 128, pontos: "1280 + 38 点券" },
    { preco: 198, pontos: "3280 + 28 点券" },
    { preco: 648, pontos: "6480 + 73 点券" },
  ];

  const handleCompra = () => {
    if (playerId && selected !== null) {
      setSuccess(true);
    }
  };

  return (
    <div className="min-h-screen bg-gradient-to-r from-purple-900 to-indigo-900 flex flex-col items-center justify-center p-6">
      {!success ? (
        <div className="w-full max-w-md p-6 bg-black/40 text-white rounded-xl shadow-lg">
          <h1 className="text-2xl font-bold mb-4 text-center">购买点券</h1>
          <input
            placeholder="请输入玩家ID"
            value={playerId}
            onChange={(e) => setPlayerId(e.target.value)}
            className="mb-4 w-full p-2 rounded bg-black/30 border border-gray-600 text-white"
          />
          <div className="space-y-3">
            {opcoes.map((op, idx) => (
              <div
                key={idx}
                className={`cursor-pointer transition p-3 rounded-xl ${
                  selected === idx ? "bg-indigo-600" : "bg-black/30"
                }`}
                onClick={() => setSelected(idx)}
              >
                <div className="flex justify-between items-center text-lg">
                  <span>{op.preco} 元</span>
                  <span>{op.pontos}</span>
                </div>
              </div>
            ))}
          </div>
          <button
            onClick={handleCompra}
            disabled={!playerId || selected === null}
            className="mt-6 w-full p-3 rounded-lg bg-green-600 hover:bg-green-700 disabled:opacity-50"
          >
            确认购买
          </button>
        </div>
      ) : (
        <div className="w-full max-w-md p-6 bg-black/40 text-white text-center rounded-xl shadow-lg">
          <h2 className="text-2xl font-bold mb-2">购买成功 ✅</h2>
          <p className="mb-2">ID: {playerId}</p>
          <p className="mb-4">收到 {opcoes[selected].pontos}</p>
          <button
            onClick={() => {
              setSuccess(false);
              setPlayerId("");
              setSelected(null);
            }}
            className="p-3 rounded-lg bg-indigo-600 hover:bg-indigo-700"
          >
            OK
          </button>
        </div>
      )}
    </div>
  );
}
