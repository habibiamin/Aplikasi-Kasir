# Aplikasi-Kasir

a. TheCashier
b. Menginput item, mentotal harga
c. 

codingan dibawah ini digunakan untuk mendeklarasikan property dari class Item.cs terdapat id, title untuk nama item, quantity untuk jumlah item, price untuk harga item, subtotal untuk total dari keseluruhan item

	private int id;
        public string title { get; set; }
        public int quantity { get; set; }
        public double price { get; set; }
        public double subtotal { get; set; }
        private string type;

        public Item(int id, string title, int quantity, string type, double price)
        {
            this.id = id;
            this.title = title;
            this.quantity = quantity;
            this.type = type;
            this.price = price;
            this.subtotal = 0;
        }

        public string getTitle()
        {
            return title;
        }
        public int getQuantity()
        {
            return quantity;
        }
        public string getType()
        {
            return type;
        }
        public double getPrice()
        {
            return price;
        }
        public double getSubTotal()
        {
            subtotal = price * quantity;
            return subtotal;
        }

method Item.cs digunakan untuk menghandle fungsi inputan user

dibawah ini adalah method Calculator.cs yang berfungsi untuk menambahkan inputan user ke dalam list dan kemudian dijumlah atau ditotal harganya


	private List<Item> listItem;
        private double total = 0;
        public Calculator()
        {
            this.listItem = new List<Item>();
        }
        public void addItem(Item item)
        {
            this.listItem.Add(item);
            this.total += item.getSubTotal();
        }
        public double getTotal()
        {
            return total;
        }
        public List<Item> getListItem()
        {
            return listItem;
        }
