local Fluent = loadstring(game:HttpGet("https://github.com/dawid-scripts/Fluent/releases/latest/download/main.lua"))()
local Window = Fluent:CreateWindow({
    Title = "anti mandrakes💀(beta) " .. Fluent.Version,
    TabWidth = 160, Size = UDim2.fromOffset(580, 460), Theme = "Dark"
})
local Tabs = {
    Main = Window:AddTab({ Title = "scripts 🍞" }),
    Settings = Window:AddTab({ Title = "configurações do hub", Icon = "settings" })
}
Tabs.Main:AddParagraph({ Title = "tema do hub", Content = "hub feito para brookhaven" })
Tabs.Main:AddParagraph({ Title = "para oq ele serve", Content = "nós esperamos q vcs q usam o hub usem contra toxicos" })
Tabs.Main:AddButton({ Title = "fly🦋", Callback =function() loadstring(game:HttpGet("https://raw.githubusercontent.com/XNEOFF/FlyGuiV3/main/FlyGuiV3.txt"))()end })
Tabs.Main:AddButton({ Title = "Dex Explorer", Callback = function()loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-Dex-Explorer-not-mine-33056"))()end })
Tabs.Main:AddButton({ Title = "infinityeld", Callback = function()loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-Infinite-Yield-31802"))()end })
 local Tabs = {
    Main = Window:AddTab({ Title = "troll" }),
    Settings = Window:AddTab({ Title = "Settings", Icon = "settings" })
}
Tabs.Main:AddButton({ Title = "tubers93 faz o L", Callback = function()loadstring(game:HttpGet("https://rawscripts.net/raw/Client-Replication-Xpress045-GUI-35134"))()end })
Tabs.Main:AddButton({ Title = "fly car", Callback = function()loadstring(game:HttpGet("https://rawscripts.net/raw/Troll-is-a-pinning-tower-2-gl1tchkidd-ui-troll-tower-reupload-45878"))()end })
Tabs.Main:AddButton({ Title = "replication UI(R6)
", Callback = function()loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-Old-Replication-UI-still-works-5477"))()end })
