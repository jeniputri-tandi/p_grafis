<img width="442" height="279" alt="Screenshot 2026-02-06 085050" src="https://github.com/user-attachments/assets/980dccb2-bb0a-4326-bcc8-6af12b7ad7f6" />

<img width="445" height="268" alt="Screenshot 2026-02-06 085059" src="https://github.com/user-attachments/assets/d861c2d3-3372-4271-ab38-d962f95e7560" />

<img width="417" height="263" alt="Screenshot 2026-02-06 085152" src="https://github.com/user-attachments/assets/f9869138-c860-4451-9b55-46af663ead8d" />

<img width="413" height="264" alt="Screenshot 2026-02-06 085159" src="https://github.com/user-attachments/assets/c779622d-af8c-46b2-b05c-c9caaca83672" />

```
import javax.swing.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

public class Aplikasi_login_sederhana extends JFrame {
    // Inisialisasi komponen sesuai tugas
    private JTextField txtUsername;
    private JPasswordField txtPassword;
    private JButton btnLogin;

    public Aplikasi_login_sederhana() {
        // Pengaturan Jendela (JFrame)
        setTitle("Aplikasi Login Sederhana");
        setSize(350, 200);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setLocationRelativeTo(null);
        setLayout(null); // Menggunakan Absolute Layout agar posisi bisa diatur manual

        // Label Username
        JLabel lblUser = new JLabel("Username:");
        lblUser.setBounds(30, 30, 80, 25);
        add(lblUser);

        // Input Username
        txtUsername = new JTextField();
        txtUsername.setBounds(120, 30, 150, 25);
        add(txtUsername);

        // Label Password
        JLabel lblPass = new JLabel("Password:");
        lblPass.setBounds(30, 70, 80, 25);
        add(lblPass);

        // Input Password
        txtPassword = new JPasswordField();
        txtPassword.setBounds(120, 70, 150, 25);
        add(txtPassword);

        // Tombol Login
        btnLogin = new JButton("Login");
        btnLogin.setBounds(120, 110, 80, 30);
        add(btnLogin);

        // --- LOGIKA VALIDASI (Inti Tugas) ---
        btnLogin.addActionListener(new ActionListener() {
            @Override
            public void actionPerformed(ActionEvent e) {
                String username = txtUsername.getText();
                String password = new String(txtPassword.getPassword());

                // Validasi If-Else
                if (username.equals("admin") && password.equals("1234")) {
                    // Pop-up Berhasil (Icon Informasi)
                    JOptionPane.showMessageDialog(null, "Login Berhasil", "Message", JOptionPane.INFORMATION_MESSAGE);
                } else {
                    // Pop-up Gagal (Icon Error/Peringatan)
                    JOptionPane.showMessageDialog(null, "Login Gagal", "Peringatan", JOptionPane.ERROR_MESSAGE);
                }
            }
        });
    }

    public static void main(String[] args) {
        // Menjalankan Aplikasi
        SwingUtilities.invokeLater(() -> {
            new Aplikasi_login_sederhana().setVisible(true);
        });
    }
}

```
