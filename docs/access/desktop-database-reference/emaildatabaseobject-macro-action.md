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
localization_priority: Normal
ms.openlocfilehash: 15cb7d6c422a9d7b0fae17ab649b6cfbc1b497a4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699918"
---
# <a name="emaildatabaseobject-macro-action"></a>EMailDatabaseObject, action de macro

**S’applique à :** Access 2013 | Office 2013

Vous pouvez utiliser l'action **EnvoyerObjetBaseDeDonnées** pour inclure une feuille de données, un formulaire, un état, un module ou une page d'accès aux données Microsoft Access spécifié dans un message électronique, dans lequel il peut être affiché ou transféré.

> [!NOTE]
> [!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. 

## <a name="settings"></a>Paramètres

L'action **EnvoyerObjetBaseDeDonnées** utilise les arguments suivants :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument de l’action</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Type d'objet</strong></p></td>
<td><p>Type d’objet à inclure dans le message électronique. Cliquez sur <strong>Table</strong> (pour une feuille de données de table), <strong>Requête</strong> (pour une feuille de données de requête), <strong>Formulaire</strong> (pour un formulaire ou une feuille de données de formulaire), <strong>État</strong>, <strong>Module</strong> ou <strong>Page d’accès aux données</strong>, <strong>Vue serveur</strong>, <strong>Procédures stockées</strong> ou <strong>Fonction</strong> dans la zone <strong>Type d’objet</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Vous ne pouvez pas envoyer de macro. Si vous voulez inclure l’objet actif, sélectionnez son type avec cet argument mais ne spécifiez aucun nom dans l’argument <strong>Nom de l’objet</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nom de l'objet</strong></p></td>
<td><p>Le nom de l’objet à inclure dans le message électronique. La zone <strong>Nom de l'objet</strong> regroupe tous les objets de la base de données ayant le type sélectionné par l'argument <strong>Type d'objet</strong>. Si vous laissez le <strong>Type d’objet</strong> et le <strong>Nom de l’objet</strong> arguments vides, Access envoie un message à l’application de messagerie sans aucun objet de base de données. Si vous exécutez une macro contenant l’action <strong>EnvoyerObjetBaseDeDonnées</strong> dans une base de données bibliothèque, Access recherche d’abord l’objet enregistré sous ce nom dans la base de données bibliothèque, puis dans la base de données active.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Format de sortie</strong></p></td>
<td><p>Le type de format à utiliser pour l’objet inclus. La liste des formats que vous pouvez choisir parmi varie selon que vous sélectionnez pour l’argument <strong>Type d’objet</strong> . Formats disponibles peuvent inclure de <strong>classeur Excel 97 - Excel 2003 (*.xls)</strong>, <strong>Classeur Excel binaire (*.xlsb)</strong>, <strong>Le classeur Excel (*.xlsx)</strong>, <strong>HTML (*.htm, * .html)</strong>, <strong>Classeur Microsoft Excel 5.0/95 (*.xls)</strong>, <strong>au Format PDF </strong>, <strong>La mise en forme de texte enrichi (*.rtf)</strong>, <strong>fichiers texte (*.txt)</strong>ou <strong>Format XPS (*.xps)</strong>. dans la zone <strong>Format de sortie</strong> . Modules peuvent être envoyés uniquement au format texte. Pages d’accès aux données peuvent uniquement être envoyés au format HTML. Si vous laissez cet argument vide, Access vous demande de spécifier le format de sortie.</p></td>
</tr>
<tr class="even">
<td><p><strong>To</strong></p></td>
<td><p>Les destinataires du message dont les noms doivent figurer sur la ligne <strong>à</strong> du message électronique. Si vous laissez cet argument vide, Access vous invite à fournir les noms des destinataires. Séparez les noms des destinataires spécifiés dans cet argument (et dans les arguments <strong>Cc</strong> et <strong>Cci</strong> ) par un point-virgule ( ;) ou avec le séparateur de liste défini sous l’onglet <strong>nombre</strong> de la boîte de dialogue <strong>Propriétés de paramètres régionaux</strong> dans Microsoft <strong>Le panneau de configuration</strong>de Windows. Si l’application de messagerie ne peut pas identifier les noms des destinataires, le message n’est pas envoyé et une erreur se produit.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cc</strong></p></td>
<td><p>Destinataires du message dont les noms doivent figurer sur la <strong>Cc</strong> (&quot;copie carbone&quot;) ligne dans le message électronique. Si vous laissez cet argument vide, la ligne <strong>Cc</strong> du message électronique est vide.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bcc</strong></p></td>
<td><p>Destinataires du message dont les noms doivent figurer sur la <strong>Cci</strong> (&quot;copie carbone invisible&quot;) ligne dans le message électronique. Si vous laissez cet argument vide, la ligne <strong>Cci</strong> du message électronique est vide.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Objet</strong></p></td>
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
<td><p><strong>Fichier de modèle</strong></p></td>
<td><p>Chemin d’accès et nom d’un fichier à utiliser comme modèle pour un fichier HTML. Le fichier modèle est un fichier contenant des balises HTML.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

L'objet inclus dans le message est au format de sortie sélectionné. Lorsque vous double-cliquez sur l'objet, le logiciel approprié s'exécute et ouvre l'objet.

Les règles suivantes sont d'application lorsque vous utilisez l'action **EnvoyerObjetBaseDeDonnées** pour inclure un objet de base de données dans un message électronique :

- Vous pouvez envoyer des feuilles de données de table, de requête et de formulaire. Dans l'objet inclus, tous les champs de la feuille de données apparaissent comme dans Access sauf ceux contenant des objets OLE. Les colonnes de ces champs sont incluses dans l'objet, mais les champs eux-mêmes sont vierges.

- Dans le cas d'un contrôle lié à un champ Oui/Non (un bouton bascule, une case d'option ou une case à cocher), le fichier de sortie affiche la valeur –1 (Oui) ou 0 (Non).

- Dans le cas d'une zone de texte liée à un champ de lien hypertexte, le fichier de sortie affiche le lien hypertexte pour tous les formats de sortie sauf le format texte MS-DOS (dans ce cas, le lien hypertexte est affiché en tant que texte normal).

- Si vous envoyez un formulaire en mode Formulaire, l'objet inclus contient la feuille de données de ce formulaire.

- Si vous envoyez un état, les seuls contrôles inclus dans l'objet sont les zones de texte et, dans certains cas, les étiquettes. Tous les autres contrôles sont ignorés de même que les informations d'en-tête et de pied de page. Il n'existe qu'une seule exception : lorsque vous envoyez un état au format Excel, une zone de texte dans un pied de page de groupe contenant une expression avec la fonction **Somme** est incluse dans l'objet. L'objet n'inclut aucun autre contrôle d'un en-tête ou pied de page (ni aucune autre fonction d'agrégation à l'exception de **Somme**).

- Des sous-états sont inclus dans l'objet.

- Lorsque vous envoyez une feuille de données, un formulaire ou une page d'accès aux données au format HTML, un fichier .html est créé et lorsque vous envoyez un rapport au format HTML, un fichier .html est créé pour chaque page du rapport.

Pour exécuter l'action **EnvoyerObjetBaseDeDonnées** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **SendObject** de l'objet **DoCmd**.

### <a name="about-the-contributor"></a>À propos du collaborateur

**Lien fourni par** Luke Chung, [FMS, Inc.](https://www.fmsinc.com/), le fondateur et président de FMS, Inc., des principaux fournisseurs de solutions de base de données personnalisée et des outils de développement.

- [Fonctionnalités et limites d’utilisation de la méthode SendObject pour envoyer](https://www.fmsinc.com/microsoftaccess/email/sendobject.html)





