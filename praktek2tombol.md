<img width="312" height="242" alt="image" src="https://github.com/user-attachments/assets/3e000c7c-72e8-4d2e-a480-4fb8e8a35710" />


<img width="323" height="229" alt="image" src="https://github.com/user-attachments/assets/f41f295b-92ca-4430-9bfc-6923fa8393f2" />


import javax.swing.*; import java.awt.event.ActionEvent; import java.awt.event.ActionListener;

public class tombolinteraktif extends javax.swing.JFrame {

    // Set judul frame
    public tombolinteraktif() {
        setTitle("tombolinteraktif");
        initComponents();
    
    // set ukuran ftame
    setSize(300, 200);
    setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    setLocationRelativeTo(null);

    // Buat JLabel
    JLabel label = new JLabel("Halo, klik tombol di bawah!");
    label.setBounds(50, 50, 250, 30);
    
    // Buat JButton
    JButton button = new JButton("Klik Saya");
    button.setBounds(50, 100, 200, 30);
    
    // Tambahkan ActionListener pada tombol
    button.addActionListener(new ActionListener() {
        @Override
        public void actionPerformed(ActionEvent e) {
            label.setText("Tombol sudah diklik!");
        }
    });
    
    // Tambahkan komponen ke frame
    add(label);
    add(button);
    
    // Set layout menjadi null agar bisa atur posisi manual
    setLayout(null);
    } //Public class di tutup di sini
   
    @SuppressWarnings("unchecked")
    // <editor-fold defaultstate="collapsed" desc="Generated Code">                          
    private void initComponents() {

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);

        javax.swing.GroupLayout layout = new javax.swing.GroupLayout(getContentPane());
        getContentPane().setLayout(layout);
        layout.setHorizontalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGap(0, 400, Short.MAX_VALUE)
        );
        layout.setVerticalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGap(0, 300, Short.MAX_VALUE)
        );

        pack();
    }// </editor-fold>                        

    public static void main(String[] args) { //Program Utama
        // Ganti Nama Objek sesuai nama kelas
        tombolinteraktif frame = new tombolinteraktif();
        frame.setVisible(true);
        
            }
}
       
    // Variables declaration - do not modify                     
    // End of variables declaration                   


