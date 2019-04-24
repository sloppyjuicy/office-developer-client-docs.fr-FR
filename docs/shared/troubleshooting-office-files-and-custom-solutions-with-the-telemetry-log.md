---
title: Dépannage des solutions personnalisées et des fichiers Office avec le journal de télémétrie
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: ef88e30e-7537-488e-bc72-8da29810f7aa
description: Utilisez le Journal de télémétrie pour Office 2013 pour déterminer les problèmes de compatibilité avec Office 2013 et les solutions élaborées pour les précédentes versions d'Office.
localization_priority: Priority
ms.openlocfilehash: 3954662a9476dca0cbb9bf4b8197979783b7e11e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346286"
---
# <a name="troubleshooting-office-files-and-custom-solutions-with-the-telemetry-log"></a>Dépannage des solutions personnalisées et des fichiers Office avec le journal de télémétrie

Utilisez le Journal de télémétrie pour Office 2013 pour déterminer les problèmes de compatibilité avec Office 2013 et les solutions élaborées pour les précédentes versions d'Office.
  
L’article suivant décrit le journal de télémétrie et explique comment l’utiliser. Pour plus d'informations sur des résultats spécifiques affichés dans le Journal de télémétrie, reportez-vous à la section [Problèmes de compatibilité dans Office](compatibility-issues-in-office.md).

Au fil des versions, Microsoft a proposé des outils et des infrastructures permettant de personnaliser, d'automatiser et d'étendre Office. Ceux-ci ont permis aux entreprises et aux utilisateurs de créer des solutions ou des compléments pour les applications Office en vue d'améliorer leur productivité et leur efficacité. Ces solutions vont des plus simples comme les macros Visual Basic for Applications (VBA) aux plus complexes telles que les personnalisations .NET Framework. La plupart des utilisateurs qui disposent de ces solutions les utilisent pour effectuer des tâches critiques parfois sans même savoir qu'ils utilisent une personnalisation ajoutée à leurs applications Office.
  
Cette prolifération de solutions Office complexifie les mises à niveau des versions Office. Les entreprises et les utilisateurs ignorent si leurs précieuses solutions sont entièrement compatibles avec la nouvelle version. Leurs solutions peuvent utiliser des fonctions et du code informatique disponibles dans des versions précédentes d'Office devenus obsolètes dans les versions ultérieures. Si une solution qui utilise une fonction obsolète est chargée dans l'application « hôte », elle risque de se comporter autrement, de générer une erreur, d'échouer au chargement, voire d'empêcher l'application hôte de fonctionner.
  
Outil reposant sur Excel 2013, le Journal de télémétrie pour Office 2013 aide les développeurs et les utilisateurs expérimentés à diagnostiquer les problèmes de compatibilité en affichant les événements qui se produisent dans un éventail d'applications Office 2013. Grâce à cet outil, les utilisateurs sont à même de déterminer les problèmes potentiels avec les compléments qu'ils utilisent dans leur environnement de travail, fournissant ainsi aux décideurs d'entreprise les informations dont ils ont besoin pour déterminer si la mise à niveau vers Office 2013 est possible. Le Journal de télémétrie propose également des commentaires détaillés sur des modifications ou des obsolescences spécifiques dans les modèles objet pour les applications Office 2013, ce qui permet aux développeurs d'identifier et de remanier rapidement le code ou les commandes problématiques. Les informaticiens peuvent voir les tendances de fonctionnement des solutions sur différents clients grâce au Tableau de bord de télémétrie pour Office 2013, outil complémentaire du Journal de télémétrie.
  
Pour plus d'informations, voir [Déployer le Tableau de bord de télémétrie](https://technet.microsoft.com/library/f69cde72-689d-421f-99b8-c51676c77717).
  
## <a name="how-the-telemetry-log-works"></a>Fonctionnement du Journal de télémétrie
<a name="OEV_Types"> </a>

Lorsqu'un fichier ou une solution Office est chargé, utilisé, fermé ou génère une erreur dans l'une des applications Office 2013 sélectionnées, celle-ci ajoute un enregistrement dans un magasin de données local (une base de données sur le même ordinateur) comprenant les informations sur l'événement. Cet enregistrement comporte le titre de l'événement, l'application qui a journalisé l'événement, l'heure, le nom du fichier ou de la solution, la gravité et une description courte des erreurs survenues, le cas échéant. Lorsqu'il est actualisé, le classeur du Journal de télémétrie affiche la liste des enregistrements que contient le magasin de données local.
  
> [!NOTE]
> L'emplacement par défaut du magasin de données local est %Users%\[utilisateur actuel]\AppData\Local\Microsoft\Office\15.0\Telemetry. La taille maximale par défaut du magasin de données est de 5 Mo (5 120 Ko). 
  
Les applications Office 2013 sélectionnées ont une API de journalisation de l'exécution qui crée un enregistrement dans le magasin de données local chaque fois qu'un fichier ou une solution déclenche l'un des événements suivants :
  
- **OnLoad**: un enregistrement est journalisé dans le magasin de données local lors du chargement d'un fichier ou d'une solution dans des applications Office 2013 spécifiques. La journalisation de l'erreur d'exécution enregistre le nom du fichier, son emplacement, ainsi que d'autres informations dans le magasin de données local lors du déclenchement d'un événement **OnLoad**. 
    
- **OnClose**: un enregistrement est journalisé lors de la fermeture d'un fichier ou d'une solution dans l'application. L'enregistrement comporte le nom du fichier ou de la solution, son emplacement et l'application qui a journalisé l'événement.
    
- **OnError**: un enregistrement est journalisé lorsqu'une erreur est détectée dans une solution pour certaines applications Office 2013. L'enregistrement comporte le nom du fichier ou de la solution, ainsi que l'échec d'exécution ou le problème de compatibilité rencontré par l'utilisateur. Dans la mesure du possible, les erreurs sont mappées sur les problèmes de compatibilité connus et s'affichent en tant que telles dans le Journal de télémétrie.
    
Le Journal de télémétrie propose des informations sur un grand nombre de types de fichiers et de solutions pour un large éventail d'applications Office 2013. Les types de fichiers et de solutions surveillés par les API de journalisation de l'exécution varient d'une application à l'autre. Voir tableau 1 pour plus d'informations sur les types de solutions surveillés.
  
### <a name="table-1-types-of-office-files-and-solutions-tracked-in-telemetry-log"></a>Tableau 1. Types de fichiers et de solutions Office suivis dans le Journal de télémétrie
<a name="OEV_Table1"> </a>

|**Type de solution**|**Applications**|**Description**|
|:-----|:-----|:-----|
|Applications de volet Office  <br/> |Excel 2013, Word 2013, Project 2013  <br/> |Il s'agit des Compléments Office hébergées dans un volet Office de l'application cliente.  <br/> |
|Applications de contenu  <br/> |Excel 2013  <br/> |Il s'agit des Compléments Office intégrées au contenu du fichier Office.  <br/> |
|Applications de messagerie  <br/> |Outlook 2013  <br/> |Il s'agit des applications qui apparaissent dans Outlook 2013 lorsque certaines conditions sont remplies (le corps ou l'objet du message comporte des mots ou des expressions spécifiques).  <br/> |
|Documents actifs  <br/> |Word 2013  <br/> PowerPoint 2013  <br/> Excel 2013  <br/> | Par « document actif », on entend tout fichier de document Office différent des autres types de solutions énumérés dans ce tableau. Il peut s'agir de ce qui suit :  <br/>  Fichiers au format binaire Office (.doc, .ppt, .pps, .xls).  <br/>  Fichiers au format OpenXML Office (.docx, .pptx, .ppsx, .xlsx).  <br/>  Fichiers prenant en charge les macros et contenant du code VBA (.docm, .dotm, .pptm, .potm, .xlsm, .xltm).  <br/>  Fichiers contenant des contrôles ActiveX.  <br/>  Fichiers comportant des connexions de données externes.  <br/> |
|Compléments COM  <br/> |Word 2013  <br/> PowerPoint 2013  <br/> Excel 2013  <br/> Outlook 2013  <br/> |Les compléments COM incluent les compléments Outils de développement Office dans Visual Studio 2010.  <br/> |
|Compléments d'automatisation Excel  <br/> |Excel 2013  <br/> |Ce type de solution inclut les versions antérieures des compléments d'automatisation pris en charge par Excel, reposant sur des compléments COM. Les fonctions des compléments d'automatisation peuvent être appelées à partir de formules dans les feuilles de calcul Excel.  <br/> |
|Macros complémentaires XLL Excel  <br/> |Excel 2013  <br/> |Les macros complémentaires XLL (.xll) sont spécifiques à Excel ; elles sont créées avec un compilateur prenant en charge la création de DLL (bibliothèques de liens dynamiques). Elles ne nécessitent pas d'installation, ni d'enregistrement. Les compléments XLL comprennent également des DLL comportant des commandes et des fonctions définies par l'utilisateur.  <br/> |
|Compléments XLS RTD Excel  <br/> |Excel 2013  <br/> |Les compléments XLS RTD (Real-Time Data) sont des feuilles de calcul Excel qui utilisent la fonction de feuille de calcul **RealTimeData** pour appeler un serveur d'automatisation afin de récupérer des données en temps réel.  <br/> |
|Compléments Word WLL  <br/> |Word 2013  <br/> |Les compléments WLL (.wll) sont spécifiques de Word et créés au moyen d’un compilateur quelconque prenant en charge la création de DLL.  <br/> |
|Compléments d'application  <br/> |Word 2013  <br/> PowerPoint 2013  <br/> Excel 2013  <br/> |Les compléments d'application sont des fichiers spécifiques à l'application qui contiennent du code VBA. Ils incluent les modèles Word prenant en charge les macros (.dotm), les compléments Excel (.xla, .xlam) et les compléments PowerPoint (.ppa, .ppam).  <br/> |
|Modèles  <br/> |Word 2013  <br/> PowerPoint 2013  <br/> Excel 2013  <br/> |Les modèles comprennent les modèles de document (.dot, .dotx), de feuille de calcul (.xlt, .xltx) ou de présentation (.pot, .potx) attachés à un fichier Office.  <br/> |
   
## <a name="using-the-office-telemetry-log"></a>Utilisation du journal de télémétrie Office
<a name="OEV_Using"> </a>

Lorsque vous installez Office 2013, le Journal de télémétrie est installé, le magasin de données local est créé sur le même ordinateur et les API de journalisation de l'exécution sont activées dans les applications Office 2013 énumérées ci-dessus. Une solution ou un fichier doit toutefois être chargé ou ouvert dans l'application pour que le Journal de télémétrie puisse commencer à le surveiller.
  
Procédez comme suit pour afficher les problèmes Office enregistrés dans le Journal de télémétrie. 
  
### <a name="to-use-the-telemetry-log"></a>Pour utiliser le Journal de télémétrie

1. Pour ouvrir le Journal de télémétrie, effectuez l'une des opérations suivantes :
    
   - **Sous Windows 7 :** dans le menu **Démarrer**, choisissez **Tous les programmes**. Dans la liste des programmes, développez **Microsoft Office 15**, développez **Outils Office 15**, puis cliquez sur **Journal de télémétrie Office 15**.
    
     Un nouveau classeur s'ouvre dans Excel 2013. Il contient trois feuilles de calcul intitulées **Événements**, **Infos système** et **Guide**.
    
   - **Sous Windows 8 :** balayez l'écran vers le haut pour afficher la barre d'applications, choisissez **Toutes les applications**, puis **Journal de télémétrie Office 15**.
    
     Un nouveau classeur s'ouvre dans Excel 2013. Il contient trois feuilles de calcul intitulées **Événements**, **Infos système** et **Guide**.
    
2. Pour afficher une liste des événements actualisée, dans la feuille de calcul **Événements**, en haut de la feuille de calcul, choisissez **Actualiser**.
    
3. Pour afficher les données d'événement recueillies dans les applications Office 2013, consultez le tableau affiché dans la feuille de calcul **Événements**. 
    
4. Pour consulter les informations relatives à l'ordinateur sur lequel Office 2013 et Journal de télémétrie sont installés, reportez-vous aux informations de la feuille de calcul **Infos système**. 
    
> [!NOTE]
> Il n'est pas nécessaire d'enregistrer le classeur Journal de télémétrie dans Excel 2013 pour conserver un enregistrement des résultats, car les informations sont enregistrées dans le magasin de données local (qui est distinct du Journal de télémétrie). Toutefois, l'enregistrement du classeur n'endommage pas le Journal de télémétrie. 
  
Le Journal de télémétrie affiche quelques informations simples sur les événements enregistrés. Chaque enregistrement affiché dans le Journal de télémétrie comporte un titre et indique la gravité de l'événement affiché. Pour les erreurs, les enregistrements comprennent également une description de l'erreur ainsi que la procédure à suivre pour la résoudre. Notez toutefois que tous les enregistrements affichés ne sont pas des erreurs occasionnées par les solutions Office ; le Journal de télémétrie indique également lorsque des solutions et des fichiers sont chargés ou fermés sans problème. 
  
Par exemple, le problème intitulé « Modèle objet - masqué : propriété Comment.Initial » apparaît si une solution ou un fichier prenant en charge les macros ouvert dans Word 2013 tente d'obtenir les initiales d'une personne ayant entré un commentaire. Word 2013 propose des fonctions de commentaires améliorées qui n'affichent pas par défaut les initiales de la personne qui a entré les commentaires. Les API associées à l'ancien modèle de commentaires ont été masquées dans le modèle d'objet Word 2013 mais restent disponibles à des fins de compatibilité descendante. Le problème « Modèle objet - masqué : propriété Comment.Initial » dans le indique le fichier qui tente d'utiliser l'API, l'application qui a déclenché l'événement (Word 2013), l'heure et la date de l'événement, ainsi qu'une description courte de l'erreur et comment la corriger.
  
**Figure 1. Journal de télémétrie Office**
  
![Observateur d’événements Office affichant des enregistrements. ] (media/off15_OfficeEventViewer_SD.png "Observateur d’événements Office affichant des enregistrements")
  
> [!NOTE]
>  La feuille de calcul des **informations système** qui se trouve dans le journal de télémétrie contient des informations sur l’ordinateur sur lequel Office 2013 est installé. La feuille de calcul affiche les informations suivantes : 
> - Nom d’utilisateur.
> - Nom complet de l’ordinateur.
> - Architecture du système d’exploitation (x64/64 bits ou x86/32 bits).
> - La version de Windows installée sur l’ordinateur.
> - Fuseau horaire pour l’horloge interne de l’ordinateur.
> - Version du journal de télémétrie.
> - Version d’Office installée sur l’ordinateur.
> 
> Ces informations peuvent être utiles lorsque vous interprétez les problèmes et les événements répertoriés dans la feuille de calcul **Événements**. 
  
Dans le Journal de télémétrie, un niveau de gravité apparaît à côté des problèmes connus. Dans l'exemple précédent, un problème dans lequel une partie du modèle d'objet a été masquée aura le plus souvent le niveau de gravité « Informationnel ». En revanche, d'autres problèmes connus peuvent être plus graves et nécessiter une action plus rapide. La gravité des problèmes affichés dans le Journal de télémétrie peut être l'une des suivantes :
  
- **Informationnel** Le problème peut ne pas avoir un effet immédiat sur la compatibilité de l'application, mais il est possible que l'utilisateur doive prendre une mesure ultérieurement. De nombreux problèmes de type « Modèle objet - masqué » ont ce niveau de gravité. 
    
- **Avertissement** Le problème peut entraîner une perte de données ou amoindrir la fidélité visuelle. 
    
- **Critique** Le problème peut occasionner une perte importante de fonctionnalité ou mener au blocage de l'application. 
    
### <a name="table-2-types-of-events-displayed-in-the-telemetry-log"></a>Tableau 2. Types d'événements affichés dans le Journal de télémétrie
<a name="OEV_Table2"> </a>

Utilisez le Tableau 2 suivant pour interpréter les enregistrements affichés dans le Journal de télémétrie.
  
|**ID d’évènement**|**Titre**|**Gravité**|**Description**|
|:-----|:-----|:-----|:-----|
|1  <br/> |Le document a été chargé  <br/> ||Le fichier indiqué dans la colonne **Fichier** a été ouvert dans l'application Office sans problème.  <br/> |
|2  <br/> |Échec de chargement du document  <br/> |Avertissement  <br/> | L'application n'a pas pu charger le fichier. Un problème de compatibilité sous-jacente est possible.  <br/><br/>Pour plus d’informations sur la façon de réparer un classeur endommagé dans Excel 2013, reportez-vous à la section [Réparation d’un classeur endommagé](https://office.microsoft.com/fr-FR/excel-help/repairing-a-corrupted-workbook-HA102749554.aspx).<br/><br/>Pour plus d'informations sur la réparation d'un document endommagé dans Word 2013, reportez-vous à la section [Enregistrer et récupérer une copie de sauvegarde d'un document](https://office.microsoft.com/fr-FR/word-help/save-and-recover-a-backup-copy-of-a-document-HA010121250.aspx). <br/> |
|3  <br/> |Le modèle a été chargé  <br/> ||Le fichier de modèle indiqué dans la colonne **Fichier** a été ouvert dans l'application Office sans problème.  <br/> |
|4  <br/> |Échec de chargement du modèle  <br/> |Avertissement  <br/> | L'application n'a pas pu charger le fichier de modèle. Un problème de compatibilité sous-jacent est possible ou la disponibilité du modèle a changé.  <br/><br/>Pour plus d’informations sur la façon de réparer un classeur endommagé dans Excel 2013, reportez-vous à la section [Réparation d’un classeur endommagé](https://office.microsoft.com/fr-FR/excel-help/repairing-a-corrupted-workbook-HA102749554.aspx).<br/><br/>Pour plus d'informations sur la réparation d'un document endommagé dans Word 2013, reportez-vous à la section [Enregistrer et récupérer une copie de sauvegarde d'un document](https://office.microsoft.com/fr-FR/word-help/save-and-recover-a-backup-copy-of-a-document-HA010121250.aspx). <br/> |
|5  <br/> |Le complément a été chargé  <br/> ||Le complément indiqué dans la colonne **Fichier** a été chargé dans l'application Office sans problème. Aucun problème de compatibilité n'a été détecté.  <br/> |
|6  <br/> |Échec du chargement du complément  <br/> |Critique  <br/> | L'application n'a pas pu charger le complément indiqué dans la colonne **Fichier**.  <br/><br/>Pour plus d’informations sur la façon de réparer un classeur endommagé dans Excel 2013, reportez-vous à la section [Réparation d’un classeur endommagé](https://office.microsoft.com/fr-FR/excel-help/repairing-a-corrupted-workbook-HA102749554.aspx). <br/><br/>  Pour plus d'informations sur la réparation d'un document endommagé dans Word 2013, reportez-vous à la section [Enregistrer et récupérer une copie de sauvegarde d'un document](https://office.microsoft.com/fr-FR/word-help/save-and-recover-a-backup-copy-of-a-document-HA010121250.aspx). <br/> |
|7  <br/> |Le manifeste du complément a été correctement téléchargé  <br/> ||L'application hôte a chargé le manifeste de l'Complément Office.  <br/> |
|8  <br/> |Échec du téléchargement du manifeste du complément  <br/> |Critique  <br/> |L’application hôte n’a pas pu charger le fichier manifeste pour l’Complément Office à partir du catalogue SharePoint, du catalogue d’entreprise ou de l’Office Store.  <br/> |
|9  <br/> |Échec de l'analyse du balisage du complément  <br/> |Critique  <br/> |L'application hôte a chargé le manifeste de l'Complément Office pour le complément, mais n'a pas pu lire le XML.  <br/> |
|10  <br/> |Le complément a trop sollicité le processeur  <br/> |Critique  <br/> |L’Complément Office a utilisé plus de 90 % des ressources du processeur sur une période de temps définie.  <br/> |
|11  <br/> |Blocage de l’application lors du chargement  <br/> |Critique  <br/> |L'application Office a tenté de charger un document ou une solution au démarrage, mais des problèmes avec le document ou la solution ont empêché l'application de démarrer.  <br/> |
|12  <br/> |L'application a du être fermée en raison d'un problème  <br/> |Critique  <br/> |Une erreur critique s'est produite dans l'application, qui a dû fermer.  <br/> |
|13  <br/> |Le document a été fermé  <br/> ||Le fichier indiqué dans la colonne **Fichier** s'est fermé sans problème.  <br/> |
|14  <br/> |La session d'application a été étendue  <br/> ||Les sessions d'application avec une solution ou un document spécifique ouvert peuvent durer au maximum 24 heures. Si une session dépasse 24 heures, l'application hôte crée une nouvelle session.  <br/> |
|15  <br/> |Le complément a été désactivé en raison de l’expiration de la recherche de chaîne  <br/> ||Les compléments de messagerie recherchent la ligne d'objet et le corps du message d'un courrier électronique pour déterminer s'ils doivent être affichés avec une expression régulière. L'application de messagerie répertoriée dans la colonne **Fichier** a été désactivée par Outlook 2013, car elle a expiré à plusieurs reprises lors d'une tentative de mise en correspondance d'une expression régulière.  <br/> |
|16  <br/> |Document ouvert lors du blocage de l’application  <br/> |Critique  <br/> |Le fichier indiqué dans la colonne **Fichier** était ouvert lorsque l'application (répertoriée dans la colonne d'application) s'est bloquée. Le fichier peut être à l'origine du blocage de l' **application**.  <br/> |
|17  <br/> |Le complément a été fermé  <br/> |Informationnel  <br/> |L'application a pu fermer le complément sans problème.  <br/> |
|18  <br/> |L'application a été fermée  <br/> ||L’application hôte a pu fermer l’Complément Office sans problème.  <br/> |
|19  <br/> |Le complément a rencontré une erreur d’exécution  <br/> |Critique  <br/> |L'Complément Office a rencontré un problème qui l'a empêchée de s'exécuter. Pour plus de détails, consultez le journal des alertes de Microsoft Office à l'aide de l'Observateur d'événements Windows sur l'ordinateur sur lequel l'erreur s'est produite.  <br/> |
|20  <br/> |Le complément n’a pas pu vérifier la licence  <br/> |Critique  <br/> |Les informations de licence de l'Complément Office n'ont pas pu être vérifiées et la licence a peut-être expiré. Pour plus de détails, consultez le journal des alertes de Microsoft Office à l'aide de l'Observateur d'événements Windows sur l'ordinateur sur lequel l'erreur s'est produite.  <br/> |
|Divers  <br/> |« Modification du comportement du modèle objet : ... »  <br/> |Informationnel  <br/> |Le code du complément ou du document prenant en charge les macros utilise un objet, un membre, une collection, une énumération ou une constante qui se comporte différemment des versions précédentes d’Office.<br/><br/> Pour plus d'informations, reportez-vous à la section [Problèmes de compatibilité dans Office](compatibility-issues-in-office.md).  <br/> |
|Divers  <br/> |« Modèle objet - supprimé : … »  <br/> |Critique  <br/> |Le code du complément ou du document prenant en charge les macros utilise une collection, une énumération, une constante, un objet ou un membre ayant été supprimé du modèle objet.<br/><br/>Pour plus d'informations, reportez-vous à la section [Problèmes de compatibilité dans Office](compatibility-issues-in-office.md).  <br/> |
|Divers  <br/> |« Modèle objet - masqué : … »  <br/> |Informationnel  <br/> |Le code du complément ou du document prenant en charge les macros utilise une collection, une énumération, une constante, un objet ou un membre ayant été masqué dans le modèle objet.<br/><br/>Pour plus d'informations, reportez-vous à la section [Problèmes de compatibilité dans Office](compatibility-issues-in-office.md).  <br/> |
|Divers  <br/> |« Contrôle : … »  <br/> ||Le fichier contient un contrôle susceptible de ne pas être pris en charge dans Office 2013 ou par le système d’exploitation de l’ordinateur.<br/><br/>Pour plus d'informations, reportez-vous à la section [Problèmes de compatibilité dans Office](compatibility-issues-in-office.md).  <br/> |
   
## <a name="conclusion"></a>Conclusion
<a name="OEV_Conclusion"> </a>

Le Journal de télémétrie fournit aux grandes entreprises, aux utilisateurs individuels et aux développeurs un outil simple pour la surveillance de leurs solutions Office critiques. En identifiant les solutions Office problématiques avant une mise à niveau à grande échelle, les entreprises peuvent prédire de manière plus raisonnable le coût que représente l'adoption d'Office 2013.
  
## <a name="see-also"></a>Voir aussi
<a name="OEV_Additional"> </a>

- [Centre pour développeurs Office](https://msdn.microsoft.com/office/aa905340.aspx)
- [Problèmes de compatibilité dans Office](compatibility-issues-in-office.md)
- [Déployer le Tableau de bord de télémétrie Office](https://technet.microsoft.com/library/f69cde72-689d-421f-99b8-c51676c77717)
- [Centre pour développeurs Office](https://msdn.microsoft.com/office/aa905340)
    

