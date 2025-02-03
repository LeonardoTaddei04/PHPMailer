# Contact Form with PHPMailer / Modulo di Contatto con PHPMailer

## English

This project is a simple contact form that uses [PHPMailer](https://github.com/PHPMailer/PHPMailer) to send emails via SMTP. The form allows users to send messages to different departments and includes basic email validation.

### Features
- Uses PHPMailer to send emails via SMTP.
- Allows users to select a department for their query.
- Provides basic validation to prevent email spoofing.
- Displays success or error messages based on form submission status.

### Prerequisites
To use this script, you need:
- A local or remote SMTP server (e.g., Gmail SMTP, SendGrid, or a self-hosted mail server).
- PHP installed with Composer.
- PHPMailer library installed via Composer.

### Installation
1. Clone this repository or copy the script into your project directory.
2. Install PHPMailer using Composer:
   ```sh
   composer require phpmailer/phpmailer
   ```
3. Configure your SMTP settings in the script (adjust `$mail->Host`, `$mail->Port`, and other settings as needed).

### Usage
1. Ensure your web server is running and can process PHP files.
2. Open `index.php` in a browser and fill out the contact form.
3. Submit the form to send an email.
4. The form will display a success or error message based on the email delivery status.

### Configuration
Modify the following parts of the script to match your needs:

- **SMTP Settings:**
  ```php
  $mail->isSMTP();
  $mail->Host = 'localhost'; // Change to your SMTP server
  $mail->Port = 80; // Change to your SMTP port
  ```
- **Sender Email:**
  ```php
  $mail->setFrom('myemail@gmail.com', '1');
  ```
- **Recipient Addresses:**
  Modify the `$addresses` array to include your desired recipients.
  ```php
  $addresses = [
      'contact' => 'contact@gmail.com',
      'myemail' => 'myemail@gmail.com',
      'accounts' => 'accounts@gmail.com',
  ];
  ```

### Security Considerations
- Never trust user-submitted email addresses directly.
- Use proper validation and sanitization to prevent header injection attacks.
- Consider implementing reCAPTCHA to prevent spam submissions.

### License
This project is licensed under the MIT License.

---

## Italiano

Questo progetto è un semplice modulo di contatto che utilizza [PHPMailer](https://github.com/PHPMailer/PHPMailer) per inviare email tramite SMTP. Il modulo consente agli utenti di inviare messaggi a diversi dipartimenti e include una validazione di base delle email.

### Caratteristiche
- Usa PHPMailer per inviare email tramite SMTP.
- Consente agli utenti di selezionare un dipartimento per la loro richiesta.
- Fornisce una validazione di base per prevenire spoofing di email.
- Mostra messaggi di successo o errore in base allo stato dell'invio del modulo.

### Prerequisiti
Per utilizzare questo script, hai bisogno di:
- Un server SMTP locale o remoto (es. Gmail SMTP, SendGrid o un server di posta auto-ospitato).
- PHP installato con Composer.
- Libreria PHPMailer installata tramite Composer.

### Installazione
1. Clona questo repository o copia lo script nella tua directory di progetto.
2. Installa PHPMailer usando Composer:
   ```sh
   composer require phpmailer/phpmailer
   ```
3. Configura le impostazioni SMTP nello script (modifica `$mail->Host`, `$mail->Port` e altre impostazioni secondo necessità).

### Utilizzo
1. Assicurati che il tuo server web sia in esecuzione e possa elaborare file PHP.
2. Apri `index.php` in un browser e compila il modulo di contatto.
3. Invia il modulo per inviare un'email.
4. Il modulo mostrerà un messaggio di successo o errore in base allo stato dell'invio dell'email.

### Configurazione
Modifica le seguenti parti dello script in base alle tue esigenze:

- **Impostazioni SMTP:**
  ```php
  $mail->isSMTP();
  $mail->Host = 'localhost'; // Cambia con il tuo server SMTP
  $mail->Port = 80; // Cambia con la tua porta SMTP
  ```
- **Email del Mittente:**
  ```php
  $mail->setFrom('myemail@gmail.com', '1');
  ```
- **Indirizzi dei Destinatari:**
  Modifica l'array `$addresses` per includere i destinatari desiderati.
  ```php
  $addresses = [
      'contact' => 'contact@gmail.com',
      'myemail' => 'myemail@gmail.com',
      'accounts' => 'accounts@gmail.com',
  ];
  ```

### Considerazioni sulla Sicurezza
- Non fidarti mai direttamente degli indirizzi email inviati dagli utenti.
- Usa una validazione e una sanitizzazione adeguata per prevenire attacchi di iniezione dell'intestazione.
- Considera l'implementazione di reCAPTCHA per prevenire invii di spam.

### Licenza
Questo progetto è concesso in licenza sotto la Licenza MIT.

