# Capstone-Kurs "Online-Wahrnehmung von Politikerinnen in der Schweiz"

Dieses _Respository_ enthält den Replikationsdatensatz für die Daten des Capstone-Kurses **"Online-Wahrnehmung von Politikerinnen in der Schweiz"**.
Im Ordner _Replikationsdatensatz_ finden sich die Codes, die die verwendeten Daten replizieren.
Die Codes sind in _R_ (Version 3.6.1) geschrieben, mit _RMarkdown_ (Version 1.2.1578) dargestellt und sowohl im _.rdm_ als auch im _.html_-Format augegeben. 
Die resultierenden Datensätze sind im R-Format _.rds_ abgespeichert. Alle benötigten Datensätze finden sich im Unterordner _Rohdaten_. Die Datenquellen sind in den Codes genannt.

&nbsp;

**Code: CS_base_draft01.rmd / CS_base_draft01.html**
+ _CS_base_draft01.rmd_ erzeugt den Basisdatensatz _df_base_draft01.rds_, in dem allgemeine Angaben wie das Geburtsjahr der Parlamentsmitglieder, das Geschlecht, etc. enthalten sind.
+ _CS_base_draft01.rmd_ benötigt die Datensätze _2019_chvote_councilofstates.csv_, _2019_chvote_nationalcouncil.csv_ und _df_parldata.rds_, die im Unterordner _Rohdaten_ abgelegt sind.

&nbsp;

**Code: CS_meta_draft01.rmd / CS_meta_draft01.html**
+ _CS_meta_draft01.rmd_ erzeugt die Metadaten des Wikipedia-Eintrags, den Datensatz _df_meta_draft01.rds_.
+ _CS_meta_draft01.rmd_ benötigt den Basisdatensatz _df_base_draft01.rds_, der entsteht, wenn _CS_base_draft01.rmd_ durchgeführt wird.

&nbsp;

**Code: CS_txt_draft01.rmd / CS_txt_draft01.html**
+ _CS_txt_draft01.rmd_ erzeugt die Inhaltsanalysedaten des Wikipedia-Eintrags, den Datensatz _df_txt_draft01.rds_. In diesem Code werden auch die Wikipediatexte heruntergeladen und verarbeitet.
+ _CS_txt_draft01.rmd_ benötigt den Basisdatensatz _df_base_draft01.rds_, der entsteht, wenn _CS_base_draft01.rmd_ durchgeführt wird.


&nbsp;

**Code: CS_alldata_draft01.rmd / CS_alldata_draft01.html**
+ _CS_alldata_draft01.rmd_ führt alle Datensätze zusammen in den Datensatz _df_alldata_draft01.rds_. 
+ _CS_alldata_draft01.rmd_ benötigt alle drei Datensätze (_df_base_draft.rds_, _df_meta_draft01.rds_ und _df_txt_draft01.rds_) die entstehen, wenn _CS_base_draft.rmd_, _CS_meta_draft.rmd_ und _CS_txt_draft01.rmd_, durchgeführt werden.

