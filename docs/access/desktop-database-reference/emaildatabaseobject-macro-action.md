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
ms.openlocfilehash: f0c0ba73274d6f27a9e2a857aea1061416168f3a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922915"
---
# <a name="emaildatabaseobject-macro-action"></a><span data-ttu-id="88133-102">EMailDatabaseObject, action de macro</span><span class="sxs-lookup"><span data-stu-id="88133-102">EMailDatabaseObject macro action</span></span>

<span data-ttu-id="88133-103">**S’applique à :** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="88133-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="88133-104">Vous pouvez utiliser l'action **EnvoyerObjetBaseDeDonnées** pour inclure une feuille de données, un formulaire, un état, un module ou une page d'accès aux données Microsoft Access spécifié dans un message électronique, dans lequel il peut être affiché ou transféré.</span><span class="sxs-lookup"><span data-stu-id="88133-104">You can use the **EMailDatabaseObject** action to include the specified Microsoft Access datasheet, form, report, module, or data access page in an electronic mail message, where it can be viewed and forwarded.</span></span>

> [!NOTE]
> <span data-ttu-id="88133-p101">[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. Pour plus d'informations sur l'activation des macros, voir les liens dans la section See Alsode cet article.</span><span class="sxs-lookup"><span data-stu-id="88133-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span>

## <a name="settings"></a><span data-ttu-id="88133-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88133-107">Settings</span></span>

<span data-ttu-id="88133-108">L'action **EnvoyerObjetBaseDeDonnées** utilise les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="88133-108">The **EMailDatabaseObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="88133-109">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="88133-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="88133-110">Description</span><span class="sxs-lookup"><span data-stu-id="88133-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88133-111"><strong>Type d'objet</strong></span><span class="sxs-lookup"><span data-stu-id="88133-111"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="88133-p102">Type d’objet à inclure dans le message électronique. Cliquez sur <strong>Table</strong> (pour une feuille de données de table), <strong>Requête</strong> (pour une feuille de données de requête), <strong>Formulaire</strong> (pour un formulaire ou une feuille de données de formulaire), <strong>État</strong>, <strong>Module</strong> ou <strong>Page d’accès aux données</strong>, <strong>Vue serveur</strong>, <strong>Procédures stockées</strong> ou <strong>Fonction</strong> dans la zone <strong>Type d’objet</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Vous ne pouvez pas envoyer de macro. Si vous voulez inclure l’objet actif, sélectionnez son type avec cet argument mais ne spécifiez aucun nom dans l’argument <strong>Nom de l’objet</strong>.</span><span class="sxs-lookup"><span data-stu-id="88133-p102">The type of object to include in the mail message. Click <strong>Table</strong> (for a table datasheet), <strong>Query</strong> (for a query datasheet), <strong>Form</strong> (for a form or form datasheet), <strong>Report</strong>, <strong>Module</strong>, or <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Stored Procedures</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You can't send a macro. If you want to include the active object, select its type with this argument, but leave the <strong>Object Name</strong> argument blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88133-116"><strong>Nom de l'objet</strong></span><span class="sxs-lookup"><span data-stu-id="88133-116"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="88133-117">Le nom de l’objet à inclure dans le message électronique.</span><span class="sxs-lookup"><span data-stu-id="88133-117">The name of the object to include in the mail message.</span></span> <span data-ttu-id="88133-118">La zone <strong>Nom de l'objet</strong> regroupe tous les objets de la base de données ayant le type sélectionné par l'argument <strong>Type d'objet</strong>.</span><span class="sxs-lookup"><span data-stu-id="88133-118">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="88133-119">Si vous laissez le <strong>Type d’objet</strong> et le <strong>Nom de l’objet</strong> arguments vides, Access envoie un message à l’application de messagerie sans aucun objet de base de données.</span><span class="sxs-lookup"><span data-stu-id="88133-119">If you leave both the <strong>Object Type</strong> and <strong>Object Name</strong> arguments blank, Access sends a message to the mail application without any database object.</span></span> <span data-ttu-id="88133-120">Si vous exécutez une macro contenant l’action <strong>EnvoyerObjetBaseDeDonnées</strong> dans une base de données bibliothèque, Access recherche d’abord l’objet enregistré sous ce nom dans la base de données bibliothèque, puis dans la base de données active.</span><span class="sxs-lookup"><span data-stu-id="88133-120">If you run a macro containing the <strong>EMailDatabaseObject</strong> action in a library database, Access looks for the object with this name first in the library database, then in the current database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88133-121"><strong>Format de sortie</strong></span><span class="sxs-lookup"><span data-stu-id="88133-121"><strong>Output Format</strong></span></span></p></td>
<td><p><span data-ttu-id="88133-122">Le type de format à utiliser pour l’objet inclus.</span><span class="sxs-lookup"><span data-stu-id="88133-122">The type of format you want used for the included object.</span></span> <span data-ttu-id="88133-123">La liste des formats que vous pouvez choisir parmi varie selon que vous sélectionnez pour l’argument <strong>Type d’objet</strong> .</span><span class="sxs-lookup"><span data-stu-id="88133-123">The list of formats you can select from will change depending on what you select for the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="88133-124">Formats disponibles peuvent inclure de <strong>classeur Excel 97 - Excel 2003 (*.xls)</strong>, <strong>Classeur Excel binaire (*.xlsb)</strong>, <strong>Le classeur Excel (*.xlsx)</strong>, <strong>HTML (*.htm, \* .html)</strong>, <strong>Classeur Microsoft Excel 5.0/95 (*.xls)</strong>, <strong>au Format PDF </strong>, <strong>La mise en forme de texte enrichi (*.rtf)</strong>, <strong>fichiers texte (*.txt)</strong>ou <strong>Format XPS (*.xps)</strong>.</span><span class="sxs-lookup"><span data-stu-id="88133-124">Available formats may include <strong>Excel 97 - Excel 2003 Workbook (*.xls)</strong>, <strong>Excel Binary Workbook (*.xlsb)</strong>, <strong>Excel Workbook (*.xlsx)</strong>, <strong>HTML (*.htm, *.html)</strong>, <strong>Microsoft Excel 5.0/95 Workbook (*.xls)</strong>, <strong>PDF Format</strong>, <strong>Rich Text Fomat (*.rtf)</strong>, <strong>Text Files (*.txt)</strong>, or <strong>XPS Format (\*.xps)</strong>.</span></span> <span data-ttu-id="88133-125">dans la zone <strong>Format de sortie</strong> .</span><span class="sxs-lookup"><span data-stu-id="88133-125">in the <strong>Output Format</strong> box.</span></span> <span data-ttu-id="88133-126">Modules peuvent être envoyés uniquement au format texte.</span><span class="sxs-lookup"><span data-stu-id="88133-126">Modules can be sent only in text format.</span></span> <span data-ttu-id="88133-127">Pages d’accès aux données peuvent uniquement être envoyés au format HTML.</span><span class="sxs-lookup"><span data-stu-id="88133-127">Data access pages can only be sent in HTML format.</span></span> <span data-ttu-id="88133-128">Si vous laissez cet argument vide, Access vous demande de spécifier le format de sortie.</span><span class="sxs-lookup"><span data-stu-id="88133-128">If you leave this argument blank, Access prompts you for the output format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88133-129"><strong>Pour</strong></span><span class="sxs-lookup"><span data-stu-id="88133-129"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="88133-130">Les destinataires du message dont les noms doivent figurer sur la ligne <strong>à</strong> du message électronique.</span><span class="sxs-lookup"><span data-stu-id="88133-130">The recipients of the message whose names you want to put on the <strong>To</strong> line in the mail message.</span></span> <span data-ttu-id="88133-131">Si vous laissez cet argument vide, Access vous invite à fournir les noms des destinataires.</span><span class="sxs-lookup"><span data-stu-id="88133-131">If you leave this argument blank, Access prompts you for the recipients' names.</span></span> <span data-ttu-id="88133-132">Séparez les noms des destinataires spécifiés dans cet argument (et dans les arguments <strong>Cc</strong> et <strong>Cci</strong> ) par un point-virgule ( ;) ou avec le séparateur de liste défini sous l’onglet <strong>nombre</strong> de la boîte de dialogue <strong>Propriétés de paramètres régionaux</strong> dans Microsoft <strong>Le panneau de configuration</strong>de Windows.</span><span class="sxs-lookup"><span data-stu-id="88133-132">Separate the recipients' names you specify in this argument (and in the <strong>Cc</strong> and <strong>Bcc</strong> arguments) with a semicolon (;) or with the list separator set on the <strong>Number</strong> tab of the <strong>Regional Settings Properties</strong> dialog box in Microsoft Windows <strong>Control Panel</strong>.</span></span> <span data-ttu-id="88133-133">Si l’application de messagerie ne peut pas identifier les noms des destinataires, le message n’est pas envoyé et une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="88133-133">If the mail application can't identify the recipients' names, the message isn't sent and an error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88133-134"><strong>Cc</strong></span><span class="sxs-lookup"><span data-stu-id="88133-134"><strong>Cc</strong></span></span></p></td>
<td><p><span data-ttu-id="88133-135">Destinataires du message dont les noms doivent figurer sur la <strong>Cc</strong> (&quot;copie carbone&quot;) ligne dans le message électronique.</span><span class="sxs-lookup"><span data-stu-id="88133-135">The message recipients whose names you want to put on the <strong>Cc</strong> (&quot;carbon copy&quot;) line in the mail message.</span></span> <span data-ttu-id="88133-136">Si vous laissez cet argument vide, la ligne <strong>Cc</strong> du message électronique est vide.</span><span class="sxs-lookup"><span data-stu-id="88133-136">If you leave this argument blank, the <strong>Cc</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88133-137"><strong>Cci</strong></span><span class="sxs-lookup"><span data-stu-id="88133-137"><strong>Bcc</strong></span></span></p></td>
<td><p><span data-ttu-id="88133-138">Destinataires du message dont les noms doivent figurer sur la <strong>Cci</strong> (&quot;copie carbone invisible&quot;) ligne dans le message électronique.</span><span class="sxs-lookup"><span data-stu-id="88133-138">The message recipients whose names you want to put on the <strong>Bcc</strong> (&quot;blind carbon copy&quot;) line in the mail message.</span></span> <span data-ttu-id="88133-139">Si vous laissez cet argument vide, la ligne <strong>Cci</strong> du message électronique est vide.</span><span class="sxs-lookup"><span data-stu-id="88133-139">If you leave this argument blank, the <strong>Bcc</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88133-140"><strong>Objet</strong></span><span class="sxs-lookup"><span data-stu-id="88133-140"><strong>Subject</strong></span></span></p></td>
<td><p><span data-ttu-id="88133-p108">Objet du message. Ce texte apparaît dans la ligne <strong>Objet</strong> du message électronique. Si vous ne spécifiez rien dans cet argument, la ligne <strong>Objet</strong> du message sera vide.</span><span class="sxs-lookup"><span data-stu-id="88133-p108">The subject of the message. This text appears on the <strong>Subject</strong> line in the mail message. If you leave this argument blank, the <strong>Subject</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88133-144"><strong>Texte du message</strong></span><span class="sxs-lookup"><span data-stu-id="88133-144"><strong>Message Text</strong></span></span></p></td>
<td><p><span data-ttu-id="88133-p109">Texte à inclure dans le message en plus de l’objet de base de données. Ce texte apparaît après l’objet dans le corps principal du message électronique. Si vous laissez cet argument vide, aucun texte supplémentaire n’est inclus dans le message. Si vous laissez les arguments <strong>Type d’objet</strong> et <strong>Nom d’objet</strong> vides, vous pouvez utiliser cet argument pour envoyer un message sans objet de base de données.</span><span class="sxs-lookup"><span data-stu-id="88133-p109">Any text you want to include in the message in addition to the database object. This text appears in the main body of the mail message, after the object. If you leave this argument blank, no additional text is included in the mail message. If you leave the <strong>Object Type</strong> and <strong>Object Name</strong> arguments blank, you can use this argument to send a mail message without a database object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88133-149"><strong>Modifier le message</strong></span><span class="sxs-lookup"><span data-stu-id="88133-149"><strong>Edit Message</strong></span></span></p></td>
<td><p><span data-ttu-id="88133-p110">Spécifie si le message peut être modifié avant d’être envoyé. Si vous sélectionnez <strong>Oui</strong>, l’application de messagerie est automatiquement lancée et le message peut être modifié. Si vous sélectionnez <strong>Non</strong>, le message est envoyé sans offrir à l’utilisateur la possibilité de modifier le message. La valeur par défaut est <strong>Oui</strong>.</span><span class="sxs-lookup"><span data-stu-id="88133-p110">Specifies whether the message can be edited before it's sent. If you select <strong>Yes</strong>, the electronic mail application starts automatically, and the message can be edited. If you select <strong>No</strong>, the message is sent without the user having a chance to edit the message. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88133-154"><strong>Fichier de modèle</strong></span><span class="sxs-lookup"><span data-stu-id="88133-154"><strong>Template File</strong></span></span></p></td>
<td><p><span data-ttu-id="88133-p111">Chemin d’accès et nom d’un fichier à utiliser comme modèle pour un fichier HTML. Le fichier modèle est un fichier contenant des balises HTML.</span><span class="sxs-lookup"><span data-stu-id="88133-p111">The path and file name of a file you want to use as a template for an HTML file. The template file is a file containing HTML tags.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="88133-157">Notes</span><span class="sxs-lookup"><span data-stu-id="88133-157">Remarks</span></span>

<span data-ttu-id="88133-p112">L'objet inclus dans le message est au format de sortie sélectionné. Lorsque vous double-cliquez sur l'objet, le logiciel approprié s'exécute et ouvre l'objet.</span><span class="sxs-lookup"><span data-stu-id="88133-p112">The object in the mail message is in the selected output format. When you double-click the object, the appropriate software starts with the object opened.</span></span>

<span data-ttu-id="88133-160">Les règles suivantes sont d'application lorsque vous utilisez l'action **EnvoyerObjetBaseDeDonnées** pour inclure un objet de base de données dans un message électronique :</span><span class="sxs-lookup"><span data-stu-id="88133-160">The following rules apply when you use the **EMailDatabaseObject** action to include a database object in a mail message:</span></span>

- <span data-ttu-id="88133-p113">Vous pouvez envoyer des feuilles de données de table, de requête et de formulaire. Dans l'objet inclus, tous les champs de la feuille de données apparaissent comme dans Access sauf ceux contenant des objets OLE. Les colonnes de ces champs sont incluses dans l'objet, mais les champs eux-mêmes sont vierges.</span><span class="sxs-lookup"><span data-stu-id="88133-p113">You can send table, query, and form datasheets. In the included object, all fields in the datasheet look as they do in Access, except fields containing OLE objects. The columns for these fields are included in the object, but the fields are blank.</span></span>

- <span data-ttu-id="88133-164">Dans le cas d'un contrôle lié à un champ Oui/Non (un bouton bascule, une case d'option ou une case à cocher), le fichier de sortie affiche la valeur –1 (Oui) ou 0 (Non).</span><span class="sxs-lookup"><span data-stu-id="88133-164">For a control bound to a Yes/No field (a toggle button, option button, or check box), the output file displays the value –1 (Yes) or 0 (No).</span></span>

- <span data-ttu-id="88133-165">Dans le cas d'une zone de texte liée à un champ de lien hypertexte, le fichier de sortie affiche le lien hypertexte pour tous les formats de sortie sauf le format texte MS-DOS (dans ce cas, le lien hypertexte est affiché en tant que texte normal).</span><span class="sxs-lookup"><span data-stu-id="88133-165">For a text box bound to a Hyperlink field, the output file displays the hyperlink for all output formats except MS-DOS text (in this case, the hyperlink is just displayed as normal text).</span></span>

- <span data-ttu-id="88133-166">Si vous envoyez un formulaire en mode Formulaire, l'objet inclus contient la feuille de données de ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="88133-166">If you send a form in Form view, the included object always contains the form's Datasheet view.</span></span>

- <span data-ttu-id="88133-p114">Si vous envoyez un état, les seuls contrôles inclus dans l'objet sont les zones de texte et, dans certains cas, les étiquettes. Tous les autres contrôles sont ignorés de même que les informations d'en-tête et de pied de page. Il n'existe qu'une seule exception : lorsque vous envoyez un état au format Excel, une zone de texte dans un pied de page de groupe contenant une expression avec la fonction **Somme** est incluse dans l'objet. L'objet n'inclut aucun autre contrôle d'un en-tête ou pied de page (ni aucune autre fonction d'agrégation à l'exception de **Somme**).</span><span class="sxs-lookup"><span data-stu-id="88133-p114">If you send a report, the only controls that are included in the object are text boxes and (in some cases) labels. All other controls are ignored. Header and footer information is also not included. The only exception to this is that when you send a report in Excel format, a text box in a group footer containing an expression with the **Sum** function is included in the object. No other control in a header or footer (and no aggregate function other than **Sum**) is included in the object.</span></span>

- <span data-ttu-id="88133-172">Des sous-états sont inclus dans l'objet.</span><span class="sxs-lookup"><span data-stu-id="88133-172">Subreports are included in the object.</span></span>

- <span data-ttu-id="88133-p115">Lorsque vous envoyez une feuille de données, un formulaire ou une page d'accès aux données au format HTML, un fichier .html est créé et lorsque vous envoyez un rapport au format HTML, un fichier .html est créé pour chaque page du rapport.</span><span class="sxs-lookup"><span data-stu-id="88133-p115">When you send a datasheet, form, or data access page in HTML format, one .html file is created. When you send a report in HTML format, one .html file is created for each page in the report.</span></span>

<span data-ttu-id="88133-175">Pour exécuter l'action **EnvoyerObjetBaseDeDonnées** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **SendObject** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="88133-175">To run the **EMailDatabaseObject** action in a Visual Basic for Applications (VBA) module, use the **SendObject** method of the **DoCmd** object.</span></span>

### <a name="about-the-contributor"></a><span data-ttu-id="88133-176">À propos du collaborateur</span><span class="sxs-lookup"><span data-stu-id="88133-176">About the contributor</span></span>

<span data-ttu-id="88133-177">**Lien fourni par** Luke Chung, [FMS, Inc.](https://www.fmsinc.com/), le fondateur et président de FMS, Inc., des principaux fournisseurs de solutions de base de données personnalisée et des outils de développement.</span><span class="sxs-lookup"><span data-stu-id="88133-177">**Link provided by** Luke Chung, [FMS, Inc.](https://www.fmsinc.com/), the founder and president of FMS, Inc., a leading provider of custom database solutions and developer tools.</span></span>

  - [<span data-ttu-id="88133-178">Fonctionnalités et limites d’utilisation de la méthode SendObject pour envoyer</span><span class="sxs-lookup"><span data-stu-id="88133-178">Features and Limits of Using the SendObject Method to Send</span></span>](https://www.fmsinc.com/microsoftaccess/email/sendobject.html)





