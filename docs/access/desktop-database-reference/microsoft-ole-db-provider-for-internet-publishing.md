---
title: Fournisseur Microsoft OLE DB pour la publication Internet
TOCTitle: Microsoft OLE DB Provider for Internet Publishing
ms:assetid: 5d1e8db5-dabb-0914-e11e-e2eac72bfa77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249327(v=office.15)
ms:contentKeyID: 48545100
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c6f1c7c65d0ac1dd2a6d3ea132a31955f175bc7f
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997482"
---
# <a name="microsoft-ole-db-provider-for-internet-publishing"></a><span data-ttu-id="b5e4e-102">Fournisseur Microsoft OLE DB pour la publication Internet</span><span class="sxs-lookup"><span data-stu-id="b5e4e-102">Microsoft OLE DB Provider for Internet Publishing</span></span>

<span data-ttu-id="b5e4e-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b5e4e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b5e4e-p101">Le fournisseur Microsoft OLE DB pour la publication Internet permet à ADO d'accéder aux ressources générées par Microsoft FrontPage ou Microsoft Internet Information Server. Les ressources incluent des fichiers source Web tels que des fichiers HTML ou des dossier Web Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b5e4e-p101">The Microsoft OLE DB Provider for Internet Publishing allows ADO to access resources served by Microsoft FrontPage or Microsoft Internet Information Server. Resources include web source files such as HTML files, or Windows 2000 web folders.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="b5e4e-106">Paramètres de chaîne de connexion</span><span class="sxs-lookup"><span data-stu-id="b5e4e-106">Connection string parameters</span></span>

<span data-ttu-id="b5e4e-107">Pour vous connecter à ce fournisseur, définissez l'argument *Provider* de la propriété [ConnectionString](connectionstring-property-ado.md) sur :</span><span class="sxs-lookup"><span data-stu-id="b5e4e-107">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSDAIPP.DSO 
```

<span data-ttu-id="b5e4e-108">Cette valeur peut également être définie ou lue à partire de la propriété [Provider](provider-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b5e4e-108">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="b5e4e-109">Chaîne de connexion classique</span><span class="sxs-lookup"><span data-stu-id="b5e4e-109">Typical connection string</span></span>

<span data-ttu-id="b5e4e-110">Voici une chaîne de connexion classique pour ce fournisseur :</span><span class="sxs-lookup"><span data-stu-id="b5e4e-110">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSDAIPP.DSO;Data Source=ResourceURL;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="b5e4e-111">\-ou -</span><span class="sxs-lookup"><span data-stu-id="b5e4e-111">\-or-</span></span>

```vb 
 
"URL=ResourceURL;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="b5e4e-112">La chaîne est composée des mots clé suivants :</span><span class="sxs-lookup"><span data-stu-id="b5e4e-112">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b5e4e-113">Mot clé</span><span class="sxs-lookup"><span data-stu-id="b5e4e-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="b5e4e-114">Description</span><span class="sxs-lookup"><span data-stu-id="b5e4e-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5e4e-115"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="b5e4e-115"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e4e-116">Spécifie le fournisseur Microsoft OLE DB pour la publication Internet.</span><span class="sxs-lookup"><span data-stu-id="b5e4e-116">Specifies the OLE DB Provider for Internet Publishing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5e4e-117"><strong>Data Source</strong> -or- <strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="b5e4e-117"><strong>Data Source</strong> -or- <strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e4e-118">Spécifie l’URL d’un fichier ou un répertoire publié dans un dossier web.</span><span class="sxs-lookup"><span data-stu-id="b5e4e-118">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5e4e-119"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="b5e4e-119"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e4e-120">Spécifie le nom de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b5e4e-120">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5e4e-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="b5e4e-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e4e-122">Spécifie le mot de passe de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b5e4e-122">Specifies the user password.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b5e4e-p102">Si vous définissez le paramètre *ResourceURL* dans la chaîne de connexion « URL= » sur une valeur non valide, le fournisseur pour la publication Internet déclenche une boîte de dialogue vous invitant à entrer une valeur valide. Ce comportement n'est pas souhaitable pour un composant de niveau intermédiaire d'une application car il interrompt l'exécution du programme jusqu'à fermeture de la boîte de dialogue et le client se fige car il n'a pas reçu de réponse du composant.</span><span class="sxs-lookup"><span data-stu-id="b5e4e-p102">If you set the *ResourceURL* value from the "URL=" in the connection string to an invalid value, by default the Internet Publishing Provider raises a dialog box to prompt for a valid value. This is undesirable behavior for a component in the middle tier of an application, because it suspends program execution until the dialog box is cleared and the client appears to freeze because it has not received a response from the component.</span></span>

> [!NOTE]
> <span data-ttu-id="b5e4e-125">Si MSDAIPP. DSO est explicitement spécifié comme valeur du fournisseur, soit avec le mot clé string de *fournisseur de* connexion ou de la propriété **Provider** , vous ne pouvez pas utiliser « URL = » dans la chaîne de connexion.</span><span class="sxs-lookup"><span data-stu-id="b5e4e-125">If MSDAIPP.DSO is explicitly specified as the value of the provider, either with the *Provider* connection string keyword or the **Provider** property, you cannot use "URL=" in the connection string.</span></span> <span data-ttu-id="b5e4e-126">Cela générerait une erreur.</span><span class="sxs-lookup"><span data-stu-id="b5e4e-126">If you do, an error will occur.</span></span> <span data-ttu-id="b5e4e-127">Vous devez simplement spécifier l'URL comme expliqué sous la rubrique [Fournisseur OLE DB pour la publication Internet](the-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="b5e4e-127">Instead, simply specify the URL as shown in the topic [Using ADO with the OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md).</span></span>

