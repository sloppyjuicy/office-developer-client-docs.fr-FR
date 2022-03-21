---
title: EMailDatabaseObject, action de macro
TOCTitle: EMailDatabaseObject macro action
ms:assetid: 7fd80596-5c08-dab9-5343-c0edc38a1af9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196469(v=office.15)
ms:contentKeyID: 48545915
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm24439
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: bd84001cde4f11dc986b6d544df7eef2b897f391
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63627626"
---
# <a name="emaildatabaseobject-macro-action"></a>EMailDatabaseObject, action de macro

**S’applique à :** Access 2013 | Office 2013

Vous pouvez utiliser l'action **EnvoyerObjetBaseDeDonnées** pour inclure une feuille de données, un formulaire, un état, un module ou une page d'accès aux données Microsoft Access spécifié dans un message électronique, dans lequel il peut être affiché ou transféré.

> [!NOTE]
> [!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. 

## <a name="settings"></a>Paramètres

L’action **EnvoyerObjetBaseDeDonnées** utilise les arguments suivants :

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument de l’action</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Type d’objet</strong></p></td>
<td><p>Type d’objet à inclure dans le message électronique. Cliquez sur <strong>Table</strong> (pour une feuille de données de table), <strong>Requête</strong> (pour une feuille de données de requête), <strong>Formulaire</strong> (pour un formulaire ou une feuille de données de formulaire), <strong>État</strong>, <strong>Module</strong> ou <strong>Page d’accès aux données</strong>, <strong>Vue serveur</strong>, <strong>Procédures stockées</strong> ou <strong>Fonction</strong> dans la zone <strong>Type d’objet</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Vous ne pouvez pas envoyer de macro. Si vous voulez inclure l’objet actif, sélectionnez son type avec cet argument mais ne spécifiez aucun nom dans l’argument <strong>Nom de l’objet</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nom de l’objet</strong></p></td>
<td><p>Nom de l’objet à inclure dans le message électronique. La zone <strong>Nom de l’objet</strong> affiche tous les objets de la base de données du type sélectionné dans l’argument <strong>Type d’objet</strong>. Si vous laissez les arguments <strong>Type d’objet</strong> et <strong>Nom d’objet</strong> vides, Access envoie un message à l’application de messagerie sans aucun objet de base de données. Si vous exécutez une macro contenant l’action <strong>EnvoyerObjetBaseDeDonnées</strong> dans une base de données bibliothèque, Access recherche d’abord l’objet enregistré sous ce nom dans la base de données bibliothèque, puis dans la base de données active.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Format de sortie</strong></p></td>
<td><p>Type de format que vous souhaitez utiliser pour l’objet inclus. La liste des formats que vous pouvez sélectionner change en fonction de ce que vous sélectionnez pour l’argument <strong>Type d’objet</strong> . Les formats disponibles peuvent inclure <strong>Excel 97 - Excel 2003 Workbook (*.xls)</strong>, <strong>Excel Binary Workbook (*.xlsb)</strong>, <strong>Excel Workbook (*.xlsx)</strong>, <strong>HTML (*.htm, *.html)</strong>, <strong>Microsoft Excel 5.0/95 Workbook (*.xls)</strong>, <strong>PDF Format</strong>, <strong>Rich Text Fomat (*.rtf)</strong>, <strong>Text Files (*.txt)</strong>, or <strong>XPS Format (*. xps)</strong>. dans la <strong>zone Format de</strong> sortie. Les modules ne peuvent être envoyés qu’au format texte. Les pages d’accès aux données peuvent uniquement être envoyées au format HTML. Si vous laissez cet argument vide, Access vous demande de spécifier le format de sortie.</p></td>
</tr>
<tr class="even">
<td><p><strong>To</strong></p></td>
<td><p>Destinataires du message dont vous souhaitez spécifier les noms dans la ligne <strong>À</strong> du message électronique. Si cet argument est vide, Access vous demande de spécifier les noms des destinataires. Séparez les noms des destinataires spécifiés dans cet argument (et dans les arguments <strong>Cc</strong> et <strong>Cci</strong>) par un point-virgule (;) ou le séparateur de listes défini dans la boîte de dialogue <strong>Personnaliser les options régionales</strong> sous l’onglet <strong>Nombres</strong> dans le <strong>Panneau de configuration</strong> de Microsoft Windows. Si l’application de messagerie ne peut pas identifier les noms des destinataires, le message n’est pas envoyé et une erreur se produit.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cc</strong></p></td>
<td><p>Destinataires du message dont vous souhaitez placer les noms sur la ligne <strong>Cc</strong> (&quot;&quot;copie carbone) du message électronique. Si vous laissez cet argument vide, la ligne <strong>Cc :</strong> du message électronique reste vide.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bcc</strong></p></td>
<td><p>Destinataires du message dont vous souhaitez placer les noms sur la ligne <strong>Bcc</strong> (&quot;&quot;copie carbone non voyante) du message électronique. Si vous laissez cet argument vide, la ligne <strong>Cci :</strong> du message électronique reste vide.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Subject</strong></p></td>
<td><p>Objet du message. Ce texte apparaît dans la ligne <strong>Objet</strong> du message électronique. Si vous ne spécifiez rien dans cet argument, la ligne <strong>Objet</strong> du message sera vide.</p></td>
</tr>
<tr class="even">
<td><p><strong>Texte du message</strong></p></td>
<td><p>Texte à inclure dans le message en plus de l’objet de base de données. Ce texte apparaît après l’objet dans le corps principal du message électronique. Si vous laissez cet argument vide, aucun texte supplémentaire n’est inclus dans le message. Si vous laissez les arguments <strong>Type d’objet</strong> et <strong>Nom d’objet</strong> vides, vous pouvez utiliser cet argument pour envoyer un message sans objet de base de données.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Modifier le message</strong></p></td>
<td><p>Spécifie si le message peut être modifié avant d’être envoyé. Si vous sélectionnez <strong>Oui</strong>, l’application de messagerie est automatiquement lancée et le message peut être modifié. Si vous sélectionnez <strong>Non</strong>, le message est envoyé sans offrir à l’utilisateur la possibilité de modifier le message. La valeur par défaut est <strong>Oui</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Fichier modèle</strong></p></td>
<td><p>Chemin d’accès et nom d’un fichier à utiliser comme modèle pour un fichier HTML. Le fichier modèle est un fichier contenant des balises HTML.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

L'objet inclus dans le message est au format de sortie sélectionné. Lorsque vous double-cliquez sur l'objet, le logiciel approprié s'exécute et ouvre l'objet.

Les règles suivantes sont d'application lorsque vous utilisez l'action **EnvoyerObjetBaseDeDonnées** pour inclure un objet de base de données dans un message électronique :

- Vous pouvez envoyer des feuilles de données de table, de requête et de formulaire. Dans l'objet inclus, tous les champs de la feuille de données apparaissent comme dans Access sauf ceux contenant des objets OLE. Les colonnes de ces champs sont incluses dans l'objet, mais les champs eux-mêmes sont vierges.

- Dans le cas d’un contrôle lié à un champ Oui/Non (un bouton bascule, une case d’option ou une case à cocher), le fichier de sortie affiche la valeur –1 (Oui) ou 0 (Non).

- Dans le cas d’une zone de texte liée à un champ de lien hypertexte, le fichier de sortie affiche le lien hypertexte pour tous les formats de sortie sauf le format texte MS-DOS (dans ce cas, le lien hypertexte est affiché en tant que texte normal).

- Si vous envoyez un formulaire en mode Formulaire, l'objet inclus contient la feuille de données de ce formulaire.

- Si vous envoyez un état, les seuls contrôles inclus dans l'objet sont les zones de texte et, dans certains cas, les étiquettes. Tous les autres contrôles sont ignorés de même que les informations d'en-tête et de pied de page. Il n'existe qu'une seule exception : lorsque vous envoyez un état au format Excel, une zone de texte dans un pied de page de groupe contenant une expression avec la fonction **Somme** est incluse dans l'objet. L'objet n'inclut aucun autre contrôle d'un en-tête ou pied de page (ni aucune autre fonction d'agrégation à l'exception de **Somme**).

- Des sous-états sont inclus dans l'objet.

- Lorsque vous envoyez une feuille de données, un formulaire ou une page d'accès aux données au format HTML, un fichier .html est créé et lorsque vous envoyez un rapport au format HTML, un fichier .html est créé pour chaque page du rapport.

Pour exécuter l'action **EnvoyerObjetBaseDeDonnées** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **SendObject** de l'objet **DoCmd**.

### <a name="about-the-contributor"></a>À propos du collaborateur

**Lien fourni par** Luke Chung, [FMS, Inc.](https://www.fmsinc.com/), le fondateur et le président de FMS, Inc., un fournisseur de premier plan de solutions de base de données personnalisées et d’outils de développement.

- [Fonctionnalités et limites de l’utilisation de la méthode SendObject pour envoyer](https://www.fmsinc.com/microsoftaccess/email/sendobject.html)





