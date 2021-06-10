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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293566"
---
# <a name="emaildatabaseobject-macro-action"></a><span data-ttu-id="32d57-102">EMailDatabaseObject, action de macro</span><span class="sxs-lookup"><span data-stu-id="32d57-102">EMailDatabaseObject macro action</span></span>

<span data-ttu-id="32d57-103">**S’applique à** : Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="32d57-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="32d57-104">Vous pouvez utiliser l'action **EnvoyerObjetBaseDeDonnées** pour inclure une feuille de données, un formulaire, un état, un module ou une page d'accès aux données Microsoft Access spécifié dans un message électronique, dans lequel il peut être affiché ou transféré.</span><span class="sxs-lookup"><span data-stu-id="32d57-104">You can use the **EMailDatabaseObject** action to include the specified Microsoft Access datasheet, form, report, module, or data access page in an electronic mail message, where it can be viewed and forwarded.</span></span>

> [!NOTE]
> <span data-ttu-id="32d57-105">[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée.</span><span class="sxs-lookup"><span data-stu-id="32d57-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="settings"></a><span data-ttu-id="32d57-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32d57-106">Settings</span></span>

<span data-ttu-id="32d57-107">L’action **EnvoyerObjetBaseDeDonnées** utilise les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="32d57-107">The **EMailDatabaseObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="32d57-108">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="32d57-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="32d57-109">Description</span><span class="sxs-lookup"><span data-stu-id="32d57-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32d57-110"><strong>Type d’objet</strong></span><span class="sxs-lookup"><span data-stu-id="32d57-110"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="32d57-p101">Type d’objet à inclure dans le message électronique. Cliquez sur <strong>Table</strong> (pour une feuille de données de table), <strong>Requête</strong> (pour une feuille de données de requête), <strong>Formulaire</strong> (pour un formulaire ou une feuille de données de formulaire), <strong>État</strong>, <strong>Module</strong> ou <strong>Page d’accès aux données</strong>, <strong>Vue serveur</strong>, <strong>Procédures stockées</strong> ou <strong>Fonction</strong> dans la zone <strong>Type d’objet</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Vous ne pouvez pas envoyer de macro. Si vous voulez inclure l’objet actif, sélectionnez son type avec cet argument mais ne spécifiez aucun nom dans l’argument <strong>Nom de l’objet</strong>.</span><span class="sxs-lookup"><span data-stu-id="32d57-p101">The type of object to include in the mail message. Click <strong>Table</strong> (for a table datasheet), <strong>Query</strong> (for a query datasheet), <strong>Form</strong> (for a form or form datasheet), <strong>Report</strong>, <strong>Module</strong>, or <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Stored Procedures</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You can't send a macro. If you want to include the active object, select its type with this argument, but leave the <strong>Object Name</strong> argument blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32d57-115"><strong>Nom de l’objet</strong></span><span class="sxs-lookup"><span data-stu-id="32d57-115"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="32d57-116">Nom de l’objet à inclure dans le message électronique.</span><span class="sxs-lookup"><span data-stu-id="32d57-116">The name of the object to include in the mail message.</span></span> <span data-ttu-id="32d57-117">La zone <strong>Nom de l’objet</strong> affiche tous les objets de la base de données du type sélectionné dans l’argument <strong>Type d’objet</strong>.</span><span class="sxs-lookup"><span data-stu-id="32d57-117">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="32d57-118">Si vous laissez les arguments <strong>Type d’objet</strong> et <strong>Nom d’objet</strong> vides, Access envoie un message à l’application de messagerie sans aucun objet de base de données.</span><span class="sxs-lookup"><span data-stu-id="32d57-118">If you leave both the <strong>Object Type</strong> and <strong>Object Name</strong> arguments blank, Access sends a message to the mail application without any database object.</span></span> <span data-ttu-id="32d57-119">Si vous exécutez une macro contenant l’action <strong>EnvoyerObjetBaseDeDonnées</strong> dans une base de données bibliothèque, Access recherche d’abord l’objet enregistré sous ce nom dans la base de données bibliothèque, puis dans la base de données active.</span><span class="sxs-lookup"><span data-stu-id="32d57-119">If you run a macro containing the <strong>EMailDatabaseObject</strong> action in a library database, Access looks for the object with this name first in the library database, then in the current database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32d57-120"><strong>Format de sortie</strong></span><span class="sxs-lookup"><span data-stu-id="32d57-120"><strong>Output Format</strong></span></span></p></td>
<td><p><span data-ttu-id="32d57-121">Type de format que vous souhaitez utiliser pour l’objet inclus.</span><span class="sxs-lookup"><span data-stu-id="32d57-121">The type of format you want used for the included object.</span></span> <span data-ttu-id="32d57-122">La liste des formats que vous pouvez sélectionner change en fonction de ce que vous sélectionnez pour <strong>l’argument Type d’objet.</strong></span><span class="sxs-lookup"><span data-stu-id="32d57-122">The list of formats you can select from will change depending on what you select for the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="32d57-123">Les formats disponibles peuvent inclure <strong>Excel 97 - Excel 2003 Workbook (*.xls),</strong> <strong>Excel Binary Workbook (*.xlsb),</strong> <strong>Excel Workbook (*.xlsx)</strong>, <strong>HTML (*.htm, *.html)</strong>, <strong>Microsoft Excel 5.0/95 Workbook (*.xls)</strong>, <strong>PDF Format</strong>, Rich Text <strong>Fomat (*.rtf)</strong>, <strong>Text Files (*.txt)</strong>ou <strong>XPS Format (\*.xps)</strong>.</span><span class="sxs-lookup"><span data-stu-id="32d57-123">Available formats may include <strong>Excel 97 - Excel 2003 Workbook (*.xls)</strong>, <strong>Excel Binary Workbook (*.xlsb)</strong>, <strong>Excel Workbook (*.xlsx)</strong>, <strong>HTML (*.htm, *.html)</strong>, <strong>Microsoft Excel 5.0/95 Workbook (*.xls)</strong>, <strong>PDF Format</strong>, <strong>Rich Text Fomat (*.rtf)</strong>, <strong>Text Files (*.txt)</strong>, or <strong>XPS Format (\*.xps)</strong>.</span></span> <span data-ttu-id="32d57-124">dans la <strong>zone Format de</strong> sortie.</span><span class="sxs-lookup"><span data-stu-id="32d57-124">in the <strong>Output Format</strong> box.</span></span> <span data-ttu-id="32d57-125">Les modules ne peuvent être envoyés qu’au format texte.</span><span class="sxs-lookup"><span data-stu-id="32d57-125">Modules can be sent only in text format.</span></span> <span data-ttu-id="32d57-126">Les pages d’accès aux données peuvent uniquement être envoyées au format HTML.</span><span class="sxs-lookup"><span data-stu-id="32d57-126">Data access pages can only be sent in HTML format.</span></span> <span data-ttu-id="32d57-127">Si vous laissez cet argument vide, Access vous demande de spécifier le format de sortie.</span><span class="sxs-lookup"><span data-stu-id="32d57-127">If you leave this argument blank, Access prompts you for the output format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32d57-128"><strong>To</strong></span><span class="sxs-lookup"><span data-stu-id="32d57-128"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="32d57-129">Destinataires du message dont vous souhaitez spécifier les noms dans la ligne <strong>À</strong> du message électronique.</span><span class="sxs-lookup"><span data-stu-id="32d57-129">The recipients of the message whose names you want to put on the <strong>To</strong> line in the mail message.</span></span> <span data-ttu-id="32d57-130">Si cet argument est vide, Access vous demande de spécifier les noms des destinataires.</span><span class="sxs-lookup"><span data-stu-id="32d57-130">If you leave this argument blank, Access prompts you for the recipients' names.</span></span> <span data-ttu-id="32d57-131">Séparez les noms des destinataires spécifiés dans cet argument (et dans les arguments <strong>Cc</strong> et <strong>Cci</strong>) par un point-virgule (;) ou le séparateur de listes défini dans la boîte de dialogue <strong>Personnaliser les options régionales</strong> sous l’onglet <strong>Nombres</strong> dans le <strong>Panneau de configuration</strong> de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="32d57-131">Separate the recipients' names you specify in this argument (and in the <strong>Cc</strong> and <strong>Bcc</strong> arguments) with a semicolon (;) or with the list separator set on the <strong>Number</strong> tab of the <strong>Regional Settings Properties</strong> dialog box in Microsoft Windows <strong>Control Panel</strong>.</span></span> <span data-ttu-id="32d57-132">Si l’application de messagerie ne peut pas identifier les noms des destinataires, le message n’est pas envoyé et une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="32d57-132">If the mail application can't identify the recipients' names, the message isn't sent and an error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32d57-133"><strong>Cc</strong></span><span class="sxs-lookup"><span data-stu-id="32d57-133"><strong>Cc</strong></span></span></p></td>
<td><p><span data-ttu-id="32d57-134">Destinataires du message dont vous souhaitez placer les noms sur la ligne <strong>Cc</strong> (copie &quot; &quot; carbone) du message électronique.</span><span class="sxs-lookup"><span data-stu-id="32d57-134">The message recipients whose names you want to put on the <strong>Cc</strong> (&quot;carbon copy&quot;) line in the mail message.</span></span> <span data-ttu-id="32d57-135">Si vous laissez cet argument vide, la ligne <strong>Cc :</strong> du message électronique reste vide.</span><span class="sxs-lookup"><span data-stu-id="32d57-135">If you leave this argument blank, the <strong>Cc</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32d57-136"><strong>Bcc</strong></span><span class="sxs-lookup"><span data-stu-id="32d57-136"><strong>Bcc</strong></span></span></p></td>
<td><p><span data-ttu-id="32d57-137">Destinataires du message dont vous souhaitez placer les noms sur la ligne <strong>Bcc</strong> (copie carbone non &quot; &quot; voyante) du message électronique.</span><span class="sxs-lookup"><span data-stu-id="32d57-137">The message recipients whose names you want to put on the <strong>Bcc</strong> (&quot;blind carbon copy&quot;) line in the mail message.</span></span> <span data-ttu-id="32d57-138">Si vous laissez cet argument vide, la ligne <strong>Cci :</strong> du message électronique reste vide.</span><span class="sxs-lookup"><span data-stu-id="32d57-138">If you leave this argument blank, the <strong>Bcc</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32d57-139"><strong>Subject</strong></span><span class="sxs-lookup"><span data-stu-id="32d57-139"><strong>Subject</strong></span></span></p></td>
<td><p><span data-ttu-id="32d57-p107">Objet du message. Ce texte apparaît dans la ligne <strong>Objet</strong> du message électronique. Si vous ne spécifiez rien dans cet argument, la ligne <strong>Objet</strong> du message sera vide.</span><span class="sxs-lookup"><span data-stu-id="32d57-p107">The subject of the message. This text appears on the <strong>Subject</strong> line in the mail message. If you leave this argument blank, the <strong>Subject</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32d57-143"><strong>Texte du message</strong></span><span class="sxs-lookup"><span data-stu-id="32d57-143"><strong>Message Text</strong></span></span></p></td>
<td><p><span data-ttu-id="32d57-p108">Texte à inclure dans le message en plus de l’objet de base de données. Ce texte apparaît après l’objet dans le corps principal du message électronique. Si vous laissez cet argument vide, aucun texte supplémentaire n’est inclus dans le message. Si vous laissez les arguments <strong>Type d’objet</strong> et <strong>Nom d’objet</strong> vides, vous pouvez utiliser cet argument pour envoyer un message sans objet de base de données.</span><span class="sxs-lookup"><span data-stu-id="32d57-p108">Any text you want to include in the message in addition to the database object. This text appears in the main body of the mail message, after the object. If you leave this argument blank, no additional text is included in the mail message. If you leave the <strong>Object Type</strong> and <strong>Object Name</strong> arguments blank, you can use this argument to send a mail message without a database object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32d57-148"><strong>Modifier le message</strong></span><span class="sxs-lookup"><span data-stu-id="32d57-148"><strong>Edit Message</strong></span></span></p></td>
<td><p><span data-ttu-id="32d57-p109">Spécifie si le message peut être modifié avant d’être envoyé. Si vous sélectionnez <strong>Oui</strong>, l’application de messagerie est automatiquement lancée et le message peut être modifié. Si vous sélectionnez <strong>Non</strong>, le message est envoyé sans offrir à l’utilisateur la possibilité de modifier le message. La valeur par défaut est <strong>Oui</strong>.</span><span class="sxs-lookup"><span data-stu-id="32d57-p109">Specifies whether the message can be edited before it's sent. If you select <strong>Yes</strong>, the electronic mail application starts automatically, and the message can be edited. If you select <strong>No</strong>, the message is sent without the user having a chance to edit the message. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32d57-153"><strong>Fichier modèle</strong></span><span class="sxs-lookup"><span data-stu-id="32d57-153"><strong>Template File</strong></span></span></p></td>
<td><p><span data-ttu-id="32d57-p110">Chemin d’accès et nom d’un fichier à utiliser comme modèle pour un fichier HTML. Le fichier modèle est un fichier contenant des balises HTML.</span><span class="sxs-lookup"><span data-stu-id="32d57-p110">The path and file name of a file you want to use as a template for an HTML file. The template file is a file containing HTML tags.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="32d57-156">Remarques</span><span class="sxs-lookup"><span data-stu-id="32d57-156">Remarks</span></span>

<span data-ttu-id="32d57-p111">L'objet inclus dans le message est au format de sortie sélectionné. Lorsque vous double-cliquez sur l'objet, le logiciel approprié s'exécute et ouvre l'objet.</span><span class="sxs-lookup"><span data-stu-id="32d57-p111">The object in the mail message is in the selected output format. When you double-click the object, the appropriate software starts with the object opened.</span></span>

<span data-ttu-id="32d57-159">Les règles suivantes sont d'application lorsque vous utilisez l'action **EnvoyerObjetBaseDeDonnées** pour inclure un objet de base de données dans un message électronique :</span><span class="sxs-lookup"><span data-stu-id="32d57-159">The following rules apply when you use the **EMailDatabaseObject** action to include a database object in a mail message:</span></span>

- <span data-ttu-id="32d57-p112">Vous pouvez envoyer des feuilles de données de table, de requête et de formulaire. Dans l'objet inclus, tous les champs de la feuille de données apparaissent comme dans Access sauf ceux contenant des objets OLE. Les colonnes de ces champs sont incluses dans l'objet, mais les champs eux-mêmes sont vierges.</span><span class="sxs-lookup"><span data-stu-id="32d57-p112">You can send table, query, and form datasheets. In the included object, all fields in the datasheet look as they do in Access, except fields containing OLE objects. The columns for these fields are included in the object, but the fields are blank.</span></span>

- <span data-ttu-id="32d57-163">Dans le cas d’un contrôle lié à un champ Oui/Non (un bouton bascule, une case d’option ou une case à cocher), le fichier de sortie affiche la valeur –1 (Oui) ou 0 (Non).</span><span class="sxs-lookup"><span data-stu-id="32d57-163">For a control bound to a Yes/No field (a toggle button, option button, or check box), the output file displays the value –1 (Yes) or 0 (No).</span></span>

- <span data-ttu-id="32d57-164">Dans le cas d’une zone de texte liée à un champ de lien hypertexte, le fichier de sortie affiche le lien hypertexte pour tous les formats de sortie sauf le format texte MS-DOS (dans ce cas, le lien hypertexte est affiché en tant que texte normal).</span><span class="sxs-lookup"><span data-stu-id="32d57-164">For a text box bound to a Hyperlink field, the output file displays the hyperlink for all output formats except MS-DOS text (in this case, the hyperlink is just displayed as normal text).</span></span>

- <span data-ttu-id="32d57-165">Si vous envoyez un formulaire en mode Formulaire, l'objet inclus contient la feuille de données de ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="32d57-165">If you send a form in Form view, the included object always contains the form's Datasheet view.</span></span>

- <span data-ttu-id="32d57-p113">Si vous envoyez un état, les seuls contrôles inclus dans l'objet sont les zones de texte et, dans certains cas, les étiquettes. Tous les autres contrôles sont ignorés de même que les informations d'en-tête et de pied de page. Il n'existe qu'une seule exception : lorsque vous envoyez un état au format Excel, une zone de texte dans un pied de page de groupe contenant une expression avec la fonction **Somme** est incluse dans l'objet. L'objet n'inclut aucun autre contrôle d'un en-tête ou pied de page (ni aucune autre fonction d'agrégation à l'exception de **Somme**).</span><span class="sxs-lookup"><span data-stu-id="32d57-p113">If you send a report, the only controls that are included in the object are text boxes and (in some cases) labels. All other controls are ignored. Header and footer information is also not included. The only exception to this is that when you send a report in Excel format, a text box in a group footer containing an expression with the **Sum** function is included in the object. No other control in a header or footer (and no aggregate function other than **Sum**) is included in the object.</span></span>

- <span data-ttu-id="32d57-171">Des sous-états sont inclus dans l'objet.</span><span class="sxs-lookup"><span data-stu-id="32d57-171">Subreports are included in the object.</span></span>

- <span data-ttu-id="32d57-p114">Lorsque vous envoyez une feuille de données, un formulaire ou une page d'accès aux données au format HTML, un fichier .html est créé et lorsque vous envoyez un rapport au format HTML, un fichier .html est créé pour chaque page du rapport.</span><span class="sxs-lookup"><span data-stu-id="32d57-p114">When you send a datasheet, form, or data access page in HTML format, one .html file is created. When you send a report in HTML format, one .html file is created for each page in the report.</span></span>

<span data-ttu-id="32d57-174">Pour exécuter l'action **EnvoyerObjetBaseDeDonnées** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **SendObject** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="32d57-174">To run the **EMailDatabaseObject** action in a Visual Basic for Applications (VBA) module, use the **SendObject** method of the **DoCmd** object.</span></span>

### <a name="about-the-contributor"></a><span data-ttu-id="32d57-175">À propos du collaborateur</span><span class="sxs-lookup"><span data-stu-id="32d57-175">About the contributor</span></span>

<span data-ttu-id="32d57-176">**Lien fourni par** Luke Chung, [FMS, Inc.,](https://www.fmsinc.com/)fondateur et président de FMS, Inc., un fournisseur de solutions de base de données personnalisées et d’outils de développement.</span><span class="sxs-lookup"><span data-stu-id="32d57-176">**Link provided by** Luke Chung, [FMS, Inc.](https://www.fmsinc.com/), the founder and president of FMS, Inc., a leading provider of custom database solutions and developer tools.</span></span>

- [<span data-ttu-id="32d57-177">Fonctionnalités et limites de l’utilisation de la méthode SendObject pour envoyer</span><span class="sxs-lookup"><span data-stu-id="32d57-177">Features and Limits of Using the SendObject Method to Send</span></span>](https://www.fmsinc.com/microsoftaccess/email/sendobject.html)





