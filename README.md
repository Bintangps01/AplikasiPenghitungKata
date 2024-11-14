
# Aplikasi Penghitung Kata

Sebuah aplikasi yang dapat digunakan untuk menghitung karakter,kata,kalimat, dan paragraf dari sebuah teks, yang ditujukan untuk menyelesaikan Tugas PBO ke-5.

#### Source Code PenghitungKataFrame.java
```

import java.awt.event.ActionEvent;
import java.io.BufferedReader;
import java.io.File;
import java.io.FileReader;
import java.io.FileWriter;
import java.io.IOException;
import javax.swing.JFileChooser;
import javax.swing.event.DocumentEvent;
import javax.swing.event.DocumentListener;

/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/GUIForms/JFrame.java to edit this template
 */

/**
 *
 * @author MyBook Z Series
 */
public class PenghitungKataFrame extends javax.swing.JFrame {

    /**
     * Creates new form PenghitungKataFrame
     */
    public PenghitungKataFrame() {
        initComponents();
        init();
    }

    /**
     * This method is called from within the constructor to initialize the form.
     * WARNING: Do NOT modify this code. The content of this method is always
     * regenerated by the Form Editor.
     */
    @SuppressWarnings("unchecked")
    // <editor-fold defaultstate="collapsed" desc="Generated Code">                          
    private void initComponents() {
        java.awt.GridBagConstraints gridBagConstraints;

        jOptionPane1 = new javax.swing.JOptionPane();
        jPanel1 = new javax.swing.JPanel();
        jScrollPane1 = new javax.swing.JScrollPane();
        textAreaInput = new javax.swing.JTextArea();
        buttonHitung = new javax.swing.JButton();
        jLabel1 = new javax.swing.JLabel();
        jLabel2 = new javax.swing.JLabel();
        jPanel2 = new javax.swing.JPanel();
        labelKarakter = new javax.swing.JLabel();
        labelKata = new javax.swing.JLabel();
        labelKalimat = new javax.swing.JLabel();
        labelParagraf = new javax.swing.JLabel();
        buttonExport = new javax.swing.JButton();
        buttonImport = new javax.swing.JButton();

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);

        jPanel1.setBackground(new java.awt.Color(153, 0, 255));
        jPanel1.setLayout(new java.awt.GridBagLayout());

        textAreaInput.setColumns(20);
        textAreaInput.setRows(5);
        jScrollPane1.setViewportView(textAreaInput);

        gridBagConstraints = new java.awt.GridBagConstraints();
        gridBagConstraints.gridx = 0;
        gridBagConstraints.gridy = 2;
        gridBagConstraints.ipadx = 200;
        gridBagConstraints.ipady = 200;
        jPanel1.add(jScrollPane1, gridBagConstraints);

        buttonHitung.setText("Hitung");
        buttonHitung.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                buttonHitungActionPerformed(evt);
            }
        });
        gridBagConstraints = new java.awt.GridBagConstraints();
        gridBagConstraints.gridx = 0;
        gridBagConstraints.gridy = 3;
        gridBagConstraints.insets = new java.awt.Insets(9, 0, 8, 0);
        jPanel1.add(buttonHitung, gridBagConstraints);

        jLabel1.setFont(new java.awt.Font("Tahoma", 1, 24)); // NOI18N
        jLabel1.setForeground(new java.awt.Color(255, 255, 255));
        jLabel1.setText("Aplikasi Penghitung Kata");
        gridBagConstraints = new java.awt.GridBagConstraints();
        gridBagConstraints.insets = new java.awt.Insets(10, 10, 10, 10);
        jPanel1.add(jLabel1, gridBagConstraints);

        jLabel2.setFont(new java.awt.Font("Segoe UI", 0, 14)); // NOI18N
        jLabel2.setForeground(new java.awt.Color(255, 255, 255));
        jLabel2.setText("Masukan Teks");
        gridBagConstraints = new java.awt.GridBagConstraints();
        gridBagConstraints.gridx = 0;
        gridBagConstraints.gridy = 1;
        gridBagConstraints.insets = new java.awt.Insets(12, 0, 12, 0);
        jPanel1.add(jLabel2, gridBagConstraints);

        jPanel2.setBorder(javax.swing.BorderFactory.createBevelBorder(javax.swing.border.BevelBorder.RAISED));
        jPanel2.setLayout(new java.awt.GridBagLayout());

        labelKarakter.setText("Jumlah Karakter :");
        gridBagConstraints = new java.awt.GridBagConstraints();
        gridBagConstraints.gridx = 0;
        gridBagConstraints.gridy = 0;
        gridBagConstraints.anchor = java.awt.GridBagConstraints.WEST;
        gridBagConstraints.insets = new java.awt.Insets(5, 20, 5, 20);
        jPanel2.add(labelKarakter, gridBagConstraints);

        labelKata.setText("Jumlah Kata :");
        gridBagConstraints = new java.awt.GridBagConstraints();
        gridBagConstraints.gridx = 0;
        gridBagConstraints.gridy = 1;
        gridBagConstraints.fill = java.awt.GridBagConstraints.HORIZONTAL;
        gridBagConstraints.anchor = java.awt.GridBagConstraints.WEST;
        gridBagConstraints.insets = new java.awt.Insets(5, 20, 5, 20);
        jPanel2.add(labelKata, gridBagConstraints);

        labelKalimat.setText("Jumlah Kalimat :");
        gridBagConstraints = new java.awt.GridBagConstraints();
        gridBagConstraints.gridx = 0;
        gridBagConstraints.gridy = 2;
        gridBagConstraints.fill = java.awt.GridBagConstraints.HORIZONTAL;
        gridBagConstraints.anchor = java.awt.GridBagConstraints.WEST;
        gridBagConstraints.insets = new java.awt.Insets(5, 20, 5, 20);
        jPanel2.add(labelKalimat, gridBagConstraints);

        labelParagraf.setText("Jumlah Paragraf");
        gridBagConstraints = new java.awt.GridBagConstraints();
        gridBagConstraints.gridx = 0;
        gridBagConstraints.gridy = 3;
        gridBagConstraints.fill = java.awt.GridBagConstraints.HORIZONTAL;
        gridBagConstraints.anchor = java.awt.GridBagConstraints.WEST;
        gridBagConstraints.insets = new java.awt.Insets(5, 20, 5, 20);
        jPanel2.add(labelParagraf, gridBagConstraints);

        gridBagConstraints = new java.awt.GridBagConstraints();
        gridBagConstraints.gridx = 0;
        gridBagConstraints.gridy = 4;
        jPanel1.add(jPanel2, gridBagConstraints);

        buttonExport.setText("Export");
        buttonExport.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                buttonExportActionPerformed(evt);
            }
        });
        gridBagConstraints = new java.awt.GridBagConstraints();
        gridBagConstraints.gridx = 0;
        gridBagConstraints.gridy = 5;
        gridBagConstraints.insets = new java.awt.Insets(6, 0, 6, 0);
        jPanel1.add(buttonExport, gridBagConstraints);

        buttonImport.setText("Import");
        buttonImport.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                buttonImportActionPerformed(evt);
            }
        });
        gridBagConstraints = new java.awt.GridBagConstraints();
        gridBagConstraints.gridx = 0;
        gridBagConstraints.gridy = 6;
        gridBagConstraints.insets = new java.awt.Insets(0, 0, 7, 0);
        jPanel1.add(buttonImport, gridBagConstraints);

        getContentPane().add(jPanel1, java.awt.BorderLayout.CENTER);

        pack();
    }// </editor-fold>                        
    private void init() {
        // Menambahkan DocumentListener pada JTextArea
        textAreaInput.getDocument().addDocumentListener(new DocumentListener() {
            @Override
            public void insertUpdate(DocumentEvent e) {
                updateResults();
            }

            @Override
            public void removeUpdate(DocumentEvent e) {
                updateResults();
            }

            @Override
            public void changedUpdate(DocumentEvent e) {
                updateResults();
            }
        });
    }
    
    // Fungsi untuk memperbarui hasil perhitungan
    private void updateResults() {
        // Ambil teks dari textAreaInput
        String text = textAreaInput.getText();

        // Menghitung jumlah kata
        int jumlahKata = hitungKata(text);

        // Menghitung jumlah karakter
        int jumlahKarakter = hitungKarakter(text);

        // Menghitung jumlah kalimat
        int jumlahKalimat = hitungKalimat(text);

        // Menghitung jumlah paragraf
        int jumlahParagraf = hitungParagraf(text);

        // Menampilkan hasil ke label
        labelKata.setText("Jumlah Kata: " + jumlahKata);
        labelKarakter.setText("Jumlah Karakter: " + jumlahKarakter);
        labelKalimat.setText("Jumlah Kalimat: " + jumlahKalimat);
        labelParagraf.setText("Jumlah Paragraf: " + jumlahParagraf);
    }
    
    private void buttonHitungActionPerformed(java.awt.event.ActionEvent evt) {                                             
        // Ambil teks dari textAreaInput
        String text = textAreaInput.getText();

        // Menghitung jumlah kata (memisahkan teks berdasarkan satu atau lebih spasi)
        int jumlahKata = hitungKata(text);

        // Menghitung jumlah karakter (tanpa menghitung spasi)
        int jumlahKarakter = hitungKarakter(text);

        // Menghitung jumlah kalimat
        int jumlahKalimat = hitungKalimat(text);

        // Menghitung jumlah paragraf
        int jumlahParagraf = hitungParagraf(text);

        // Menampilkan hasil ke label
        labelKata.setText("Jumlah Kata: " + jumlahKata);
        labelKarakter.setText("Jumlah Karakter: " + jumlahKarakter);
        labelKalimat.setText("Jumlah Kalimat: " + jumlahKalimat);
        labelParagraf.setText("Jumlah Paragraf: " + jumlahParagraf);
    }                                            

    private void buttonExportActionPerformed(java.awt.event.ActionEvent evt) {                                             
        // Membuka JFileChooser untuk memilih lokasi dan nama file
        JFileChooser fileChooser = new JFileChooser();
        fileChooser.setDialogTitle("Pilih Lokasi dan Nama File");

        // Menentukan filter untuk file teks (.txt)
        fileChooser.setFileFilter(new javax.swing.filechooser.FileNameExtensionFilter("File Teks (*.txt)", "txt"));
        
        // Menampilkan JFileChooser dan menangani aksi pengguna
        int userSelection = fileChooser.showSaveDialog(this);
        
        if (userSelection == JFileChooser.APPROVE_OPTION) {
            File fileToSave = fileChooser.getSelectedFile();

            // Jika file tidak berakhiran .txt, tambahkan ekstensi .txt secara otomatis
            if (!fileToSave.getName().endsWith(".txt")) {
                fileToSave = new File(fileToSave.getAbsolutePath() + ".txt");
            }

            try (FileWriter writer = new FileWriter(fileToSave)) {
                // Menulis teks dari textAreaInput ke file
                String text = textAreaInput.getText();
                writer.write("Teks yang Dimasukkan:\n\n" + text + "\n\n");
                writer.write("Hasil Penghitungan:\n");
                writer.write("Jumlah Kata: " + labelKata.getText() + "\n");
                writer.write("Jumlah Karakter: " + labelKarakter.getText() + "\n");
                writer.write("Jumlah Kalimat: " + labelKalimat.getText() + "\n");
                writer.write("Jumlah Paragraf: " + labelParagraf.getText() + "\n");

                // Menampilkan pesan sukses
                jOptionPane1.showMessageDialog(this, "Data berhasil diekspor ke: " + fileToSave.getAbsolutePath());
            } catch (IOException ex) {
                // Menangani error jika gagal menulis ke file
                jOptionPane1.showMessageDialog(this, "Terjadi kesalahan saat menyimpan file.\n" + ex.getMessage());
            }
        }
    }                                            

    private void buttonImportActionPerformed(java.awt.event.ActionEvent evt) {                                             
        // Membuka JFileChooser untuk memilih file
        JFileChooser fileChooser = new JFileChooser();
        fileChooser.setDialogTitle("Pilih File yang Akan Diimpor");
        fileChooser.setFileFilter(new javax.swing.filechooser.FileNameExtensionFilter("File Teks (*.txt)", "txt"));

        // Menampilkan dialog untuk memilih file
        int userSelection = fileChooser.showOpenDialog(this);

        if (userSelection == JFileChooser.APPROVE_OPTION) {
            File fileToOpen = fileChooser.getSelectedFile();

            // Membaca isi file dan menampilkannya di textAreaInput
            try (BufferedReader reader = new BufferedReader(new FileReader(fileToOpen))) {
                StringBuilder text = new StringBuilder();
                String line;
                while ((line = reader.readLine()) != null) {
                    text.append(line).append("\n");
                }
                textAreaInput.setText(text.toString()); // Mengisi textArea dengan konten file

                // Menampilkan pesan bahwa file berhasil diimpor
                jOptionPane1.showMessageDialog(this, "File berhasil diimpor: " + fileToOpen.getAbsolutePath());
                updateResults(); // Memperbarui hasil penghitungan setelah file dimuat
            } catch (IOException ex) {
                // Menangani error jika file tidak dapat dibaca
                jOptionPane1.showMessageDialog(this, "Terjadi kesalahan saat membaca file.\n" + ex.getMessage());
            }
        }
    }                                            

    public void hitungJumlah(String text) {
        // Menghitung jumlah kata
        int jumlahKata = hitungKata(text);
        // Menghitung jumlah karakter
        int jumlahKarakter = hitungKarakter(text);
        // Menghitung jumlah kalimat
        int jumlahKalimat = hitungKalimat(text);
        // Menghitung jumlah paragraf
        int jumlahParagraf = hitungParagraf(text);

        // Menampilkan hasil pada label
        labelKata.setText("Jumlah Kata: " + jumlahKata);
        labelKarakter.setText("Jumlah Karakter: " + jumlahKarakter);
        labelKalimat.setText("Jumlah Kalimat: " + jumlahKalimat);
        labelParagraf.setText("Jumlah Paragraf: " + jumlahParagraf);
    }
    
    // Fungsi untuk menghitung jumlah kata (spasi tidak dihitung sebagai kata)
    public int hitungKata(String text) {
        // Menghilangkan spasi berlebih dan menghitung kata
        if (text.trim().isEmpty()) return 0;
        String[] kata = text.trim().split("\\s+");
        return kata.length;
    }

    // Fungsi untuk menghitung jumlah karakter (spasi tidak dihitung)
    public int hitungKarakter(String text) {
        // Menghilangkan semua spasi dan menghitung jumlah karakter
        String textWithoutSpaces = text.replaceAll("\\s+", "");
        return textWithoutSpaces.length();
    }

    // Fungsi untuk menghitung jumlah kalimat
    public int hitungKalimat(String text) {
        if (text.trim().isEmpty()) return 0;
        // Menghitung kalimat berdasarkan tanda titik, tanda seru, atau tanda tanya
        String[] kalimat = text.split("[.!?]");
        return kalimat.length;
    }
    
    // Fungsi untuk menghitung jumlah paragraf
    public int hitungParagraf(String text) {
        if (text.trim().isEmpty()) return 0;
        // Menghitung paragraf berdasarkan baris kosong
        String[] paragraf = text.split("\\n\\s*\\n");
        return paragraf.length;
    }
    
    // Event handler untuk tombol hitung
    public void tombolHitungActionPerformed(ActionEvent e) {
        // Ambil teks dari TextArea
        String text = textAreaInput.getText();
        // Panggil fungsi untuk menghitung dan update label
        hitungJumlah(text);
    }
    /**
     * @param args the command line arguments
     */
    public static void main(String args[]) {
        /* Set the Nimbus look and feel */
        //<editor-fold defaultstate="collapsed" desc=" Look and feel setting code (optional) ">
        /* If Nimbus (introduced in Java SE 6) is not available, stay with the default look and feel.
         * For details see http://download.oracle.com/javase/tutorial/uiswing/lookandfeel/plaf.html 
         */
        try {
            for (javax.swing.UIManager.LookAndFeelInfo info : javax.swing.UIManager.getInstalledLookAndFeels()) {
                if ("Nimbus".equals(info.getName())) {
                    javax.swing.UIManager.setLookAndFeel(info.getClassName());
                    break;
                }
            }
        } catch (ClassNotFoundException ex) {
            java.util.logging.Logger.getLogger(PenghitungKataFrame.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (InstantiationException ex) {
            java.util.logging.Logger.getLogger(PenghitungKataFrame.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (IllegalAccessException ex) {
            java.util.logging.Logger.getLogger(PenghitungKataFrame.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (javax.swing.UnsupportedLookAndFeelException ex) {
            java.util.logging.Logger.getLogger(PenghitungKataFrame.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        }
        //</editor-fold>

        /* Create and display the form */
        java.awt.EventQueue.invokeLater(new Runnable() {
            public void run() {
                new PenghitungKataFrame().setVisible(true);
            }
        });
    }

    // Variables declaration - do not modify                     
    private javax.swing.JButton buttonExport;
    private javax.swing.JButton buttonHitung;
    private javax.swing.JButton buttonImport;
    private javax.swing.JLabel jLabel1;
    private javax.swing.JLabel jLabel2;
    private javax.swing.JOptionPane jOptionPane1;
    private javax.swing.JPanel jPanel1;
    private javax.swing.JPanel jPanel2;
    private javax.swing.JScrollPane jScrollPane1;
    private javax.swing.JLabel labelKalimat;
    private javax.swing.JLabel labelKarakter;
    private javax.swing.JLabel labelKata;
    private javax.swing.JLabel labelParagraf;
    private javax.swing.JTextArea textAreaInput;
    // End of variables declaration                   
}
```
## Fitur Utama
- Menghitung Kata dan Karakter pada suatu teks
- Perhitungan Dilakukan secara real time

## Fitur Tambahan (Variasi)
- Menghitung jumlah kalimat dan paragraf
- opsi export dan import hasil
## Referensi

 - [Modul PBO2 Tugas 5](https://drive.google.com/file/d/1142tmuIMPH-T0PHFhoWhXhbNw6-9QVpc/view)


## Biodata Pembuat
- Nama : Bintang Putra Setiawan
- Kelas : 5B Reg Pagi Banjarmasin
- NPM : 2210010539
- [@Bintangps01](https://github.com/Bintangps01)