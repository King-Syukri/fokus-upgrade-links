# Mapping nama produk ke URL afiliasi Bang Syukri
product_links = {
    "The Genius Wave": "https://forgeniuswave.com/DSvsl/#aff=Kingsyukri",
    "The Billionaire Brain Wave": "https://digistore24.com/redir/434768/Kingsyukri/",
    "Astral Brainwave": "https://astralhq.com/brainwave/#a_aid=Kingsyukri",
    "TeslaCare BioHealing": "https://digistore24.com/redir/484654/Kingsyukri/",
    "EMF Protection Shield": "https://digistore24.com/redir/484661/Kingsyukri/",
    "Advanced BioNutritionals": "https://digistore24.com/redir/484657/Kingsyukri/",
    "Systeme.io Gratis": "https://systeme.io/id?sa=sa0239241355225eed1dccab11d415c33575fdf932"
}

# Urutan nama produk sesuai permintaan (333 urutan, pola berulang)
product_names = list(product_links.keys())
total_links = 333
html_links = []

for i in range(total_links):
    name = product_names[i % len(product_names)]
    url = product_links[name]
    html_links.append(f'<a href="{url}" rel="nofollow" target="_blank">{name} #{i + 1}</a>')

# Gabungkan ke dalam satu file HTML
html_output = "<!-- Generated Backlinks -->\n<div>\n" + "\n".join(html_links) + "\n</div>"
file_path = "/mnt/data/backlinks_333.html"
with open(file_path, "w") as f:
    f.write(html_output)

file_path
