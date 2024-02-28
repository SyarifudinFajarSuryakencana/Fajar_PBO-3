
// Class Mobil
class Mobil {
    private String merek;
    private String warna;
    
    public Mobil(String merek, String warna) {
        this.merek = merek;
        this.warna = warna;
    }
    
    public void infoMobil() {
        System.out.println("Merek: " + merek);
        System.out.println("Warna: " + warna);
    }
}

// Class MobilDiesel yang merupakan turunan dari class Mobil
class MobilDiesel extends Mobil {
    private int kapasitasTangki;
    
    public MobilDiesel(String merek, String warna, int kapasitasTangki) {
        super(merek, warna);
        this.kapasitasTangki = kapasitasTangki;
    }
    
    public void infoMobilDiesel() {
        super.infoMobil();
        System.out.println("Kapasitas Tangki: " + kapasitasTangki + " liter");
    }
}

// Class MobilBensin yang merupakan turunan dari class Mobil
class MobilBensin extends Mobil {
    private int konsumsiBBM;
    
    public MobilBensin(String merek, String warna, int konsumsiBBM) {
        super(merek, warna);
        this.konsumsiBBM = konsumsiBBM;
    }
    
    public void infoMobilBensin() {
        super.infoMobil();
        System.out.println("Konsumsi BBM: " + konsumsiBBM + " km/liter");
    }
}

// Class Main
public class Main {
    public static void main(String[] args) {
        MobilDiesel mobilDiesel = new MobilDiesel("Toyota", "Hitam", 50);
        mobilDiesel.infoMobilDiesel();
        
        System.out.println();
        
        MobilBensin mobilBensin = new MobilBensin("Honda", "Merah", 15);
        mobilBensin.infoMobilBensin();
    }
}
 
