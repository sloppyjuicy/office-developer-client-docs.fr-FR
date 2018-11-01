---
title: Fournisseur Microsoft OLE DB pour la publication Internet
TOCTitle: Microsoft OLE DB Provider for Internet Publishing
ms:assetid: 5d1e8db5-dabb-0914-e11e-e2eac72bfa77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249327(v=office.15)
ms:contentKeyID: 48545100
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bb0bb40d0f12bd9d5a6c8b29af1d4e27d806db87
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882083"
---
# <a name="microsoft-ole-db-provider-for-internet-publishing"></a><span data-ttu-id="052f3-102">Fournisseur Microsoft OLE DB pour la publication Internet</span><span class="sxs-lookup"><span data-stu-id="052f3-102">Microsoft OLE DB Provider for Internet Publishing</span></span>

<span data-ttu-id="052f3-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="052f3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="052f3-p101">Le fournisseur Microsoft OLE DB pour la publication Internet permet à ADO d'accéder aux ressources générées par Microsoft FrontPage ou Microsoft Internet Information Server. Les ressources incluent des fichiers source Web tels que des fichiers HTML ou des dossier Web Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="052f3-p101">The Microsoft OLE DB Provider for Internet Publishing allows ADO to access resources served by Microsoft FrontPage or Microsoft Internet Information Server. Resources include web source files such as HTML files, or Windows 2000 web folders.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="052f3-106">Paramètres de la chaîne de connexion</span><span class="sxs-lookup"><span data-stu-id="052f3-106">Connection String Parameters</span></span>

<span data-ttu-id="052f3-107">Pour vous connecter à ce fournisseur, définissez l'argument *Provider* de la propriété [ConnectionString](connectionstring-property-ado.md) sur :</span><span class="sxs-lookup"><span data-stu-id="052f3-107">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSDAIPP.DSO 
```

<span data-ttu-id="052f3-108">Cette valeur peut également être définie ou lue à partire de la propriété [Provider](provider-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="052f3-108">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="052f3-109">Chaîne de connexion classique</span><span class="sxs-lookup"><span data-stu-id="052f3-109">Typical Connection String</span></span>

<span data-ttu-id="052f3-110">Voici une chaîne de connexion classique pour ce fournisseur :</span><span class="sxs-lookup"><span data-stu-id="052f3-110">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSDAIPP.DSO;Data Source=ResourceURL;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="052f3-111">\-ou -</span><span class="sxs-lookup"><span data-stu-id="052f3-111">\-or-</span></span>

```vb 
 
"URL=ResourceURL;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="052f3-112">La chaîne est composée des mots clé suivants :</span><span class="sxs-lookup"><span data-stu-id="052f3-112">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="052f3-113">Mot clé</span><span class="sxs-lookup"><span data-stu-id="052f3-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="052f3-114">Description</span><span class="sxs-lookup"><span data-stu-id="052f3-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="052f3-115"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="052f3-115"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="052f3-116">Spécifie le fournisseur Microsoft OLE DB pour la publication Internet.</span><span class="sxs-lookup"><span data-stu-id="052f3-116">Specifies the OLE DB Provider for Internet Publishing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="052f3-117"><strong>Data Source</strong> -or- <strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="052f3-117"><strong>Data Source</strong> -or- <strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="052f3-118">Spécifie l’URL d’un fichier ou un répertoire publié dans un dossier web.</span><span class="sxs-lookup"><span data-stu-id="052f3-118">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="052f3-119"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="052f3-119"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="052f3-120">Spécifie le nom de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="052f3-120">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="052f3-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="052f3-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="052f3-122">Spécifie le mot de passe de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="052f3-122">Specifies the user password.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="052f3-p102">Si vous définissez le paramètre *ResourceURL* dans la chaîne de connexion « URL= » sur une valeur non valide, le fournisseur pour la publication Internet déclenche une boîte de dialogue vous invitant à entrer une valeur valide. Ce comportement n'est pas souhaitable pour un composant de niveau intermédiaire d'une application car il interrompt l'exécution du programme jusqu'à fermeture de la boîte de dialogue et le client se fige car il n'a pas reçu de réponse du composant.</span><span class="sxs-lookup"><span data-stu-id="052f3-p102">If you set the *ResourceURL* value from the "URL=" in the connection string to an invalid value, by default the Internet Publishing Provider raises a dialog box to prompt for a valid value. This is undesirable behavior for a component in the middle tier of an application, because it suspends program execution until the dialog box is cleared and the client appears to freeze because it has not received a response from the component.</span></span>


> [!NOTE]
> <P><span data-ttu-id="052f3-125">Si MSDAIPP. DSO est explicitement spécifié comme valeur du fournisseur, soit avec le mot clé string de <EM>fournisseur de</EM> connexion ou de la propriété <STRONG>Provider</STRONG> , vous ne pouvez pas utiliser « URL = » dans la chaîne de connexion.</span><span class="sxs-lookup"><span data-stu-id="052f3-125">If MSDAIPP.DSO is explicitly specified as the value of the provider, either with the <EM>Provider</EM> connection string keyword or the <STRONG>Provider</STRONG> property, you cannot use "URL=" in the connection string.</span></span> <span data-ttu-id="052f3-126">Cela générerait une erreur.</span><span class="sxs-lookup"><span data-stu-id="052f3-126">If you do, an error will occur.</span></span> <span data-ttu-id="052f3-127">Vous devez simplement spécifier l'URL comme expliqué sous la rubrique <A href="the-ole-db-provider-for-internet-publishing.md">Fournisseur OLE DB pour la publication Internet</A>.</span><span class="sxs-lookup"><span data-stu-id="052f3-127">Instead, simply specify the URL as shown in the topic <A href="the-ole-db-provider-for-internet-publishing.md">Using ADO with the OLE DB Provider for Internet Publishing</A>.</span></span></P>


