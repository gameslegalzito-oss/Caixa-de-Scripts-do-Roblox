# Caixa-de-Scripts-do-Roblox
Uma Caixa com tabelas de todos os Scripts para você usar no Roblox 
-- Criar GUI para "Char Me"
local Players = game:GetService("Players")
local player = Players.LocalPlayer

-- Criar a GUI
local screenGui = Instance.new("ScreenGui", player:WaitForChild("PlayerGui"))
screenGui.Name = "CharMeGUI"

local frame = Instance.new("Frame", screenGui)
frame.Size = UDim2.new(0, 300, 0, 150)
frame.Position = UDim2.new(0.5, -150, 0.5, -75)
frame.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
frame.BorderSizePixel = 0

local nameBox = Instance.new("TextBox", frame)
nameBox.PlaceholderText = "Nome do jogador"
nameBox.Size = UDim2.new(1, -20, 0, 30)
nameBox.Position = UDim2.new(0, 10, 0, 10)
nameBox.Text = ""
nameBox.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
nameBox.TextColor3 = Color3.fromRGB(255, 255, 255)

local msgBox = Instance.new("TextBox", frame)
msgBox.PlaceholderText = "Mensagem"
msgBox.Size = UDim2.new(1, -20, 0, 30)
msgBox.Position = UDim2.new(0, 10, 0, 50)
msgBox.Text = ""
msgBox.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
msgBox.TextColor3 = Color3.fromRGB(255, 255, 255)

local button = Instance.new("TextButton", frame)
button.Text = "Fingir"
button.Size = UDim2.new(1, -20, 0, 30)
button.Position = UDim2.new(0, 10, 0, 90)
button.BackgroundColor3 = Color3.fromRGB(70, 130, 180)
button.TextColor3 = Color3.fromRGB(255, 255, 255)

-- Função para "fingir" chat
button.MouseButton1Click:Connect(function()
	local fakeName = nameBox.Text
	local message = msgBox.Text

	if fakeName ~= "" and message ~= "" then
		local ChatService = require(game:GetService("ReplicatedStorage"):WaitForChild("ChatServiceRunner"):WaitForChild("ChatService"))

		-- Cria uma mensagem falsa localmente
		game:GetService("StarterGui"):SetCore("ChatMakeSystemMessage", {
			Text = fakeName .. ": " .. message,
			Color = Color3.fromRGB(255, 255, 255),
			Font = Enum.Font.SourceSansBold,
			TextSize = 18
		})
	end
end)
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Scripts de Roblox</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>📜 Scripts de Roblox</h1>
        <p>Vários scripts úteis para Roblox! Clique para copiar.</p>
    </header>

    <main id="script-list">
        <!-- Os scripts serão adicionados via scripts.js -->
    </main>

    <footer>
        <p>Feito por [Seu Nome ou Nick] - © 2025</p>
    </footer>

    <script src="scripts.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    background-color: #1e1e1e;
    color: white;
    margin: 0;
    padding: 0;
}

header {
    background-color: #20232a;
    padding: 20px;
    text-align: center;
}

main {
    padding: 20px;
}

.script-card {
    background-color: #2c2f33;
    padding: 15px;
    margin-bottom: 15px;
    border-radius: 8px;
}

.script-card pre {
    background-color: #1e1e1e;
    padding: 10px;
    overflow-x: auto;
    border: 1px solid #333;
    border-radius: 4px;
}

button {
    margin-top: 10px;
    background-color: #7289da;
    color: white;
    padding: 8px 12px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

button:hover {
    background-color: #5b6eae;
}

footer {
    text-align: center;
    padding: 15px;
    background-color: #20232a;
    position: fixed;

    
    width: 100%;
    bottom: 0;
}
body {
    font-family: Arial, sans-serif;
    background-color: #1e1e1e;
    color: white;
    margin: 0;
    padding: 0;
}

header {
    background-color: #20232a;
    padding: 20px;
    text-align: center;
}

main {
    padding: 20px;
}

.script-card {
    background-color: #2c2f33;
    padding: 15px;
    margin-bottom: 15px;
    border-radius: 8px;
}

.script-card pre {
    background-color: #1e1e1e;
    padding: 10px;
    overflow-x: auto;
    border: 1px solid #333;
    border-radius: 4px;
}

button {
    margin-top: 10px;
    background-color: #7289da;
    color: white;
    padding: 8px 12px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

button:hover {
    background-color: #5b6eae;
}

footer {
    text-align: center;
    padding: 15px;
    background-color: #20232a;
    position: fixed;
    width: 100%;
    bottom: 0;
}



