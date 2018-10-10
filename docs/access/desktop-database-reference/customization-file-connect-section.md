---
title: Section Connect du fichier de personnalisation
TOCTitle: Customization File Connect Section
ms:assetid: 037abfb4-798d-4b09-6133-356969aee95c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248802(v=office.15)
ms:contentKeyID: 48542985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dd4b7eed3cb5d8192866127322c00e7ecd5a15b5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470941"
---
# <a name="customization-file-connect-section"></a><span data-ttu-id="e01d3-102">Section Connect du fichier de personnalisation</span><span class="sxs-lookup"><span data-stu-id="e01d3-102">Customization File Connect Section</span></span>

<span data-ttu-id="e01d3-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e01d3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e01d3-p101">Le comportement par défaut du gestionnaire est de refuser toutes les connexions. La section **connect** indique les exceptions à ce comportement. Par exemple, si toutes les sections **connect** sont absentes ou vides, par défaut, aucune connexion ne peut être établie.</span><span class="sxs-lookup"><span data-stu-id="e01d3-p101">The default behavior of the handler is to deny all connections. The **connect** section specifies exceptions to that behavior. For example, if all the **connect** sections were absent or empty, then by default no connections could be made.</span></span>

<span data-ttu-id="e01d3-107">La section **connect** peut contenir :</span><span class="sxs-lookup"><span data-stu-id="e01d3-107">The **connect** section can contain:</span></span>

- <span data-ttu-id="e01d3-p102">une entrée d'accès par défaut qui spécifie les opérations de lecture et d'écriture autorisées par défaut sur cette connexion. Si aucune entrée d'accès par défaut n'existe dans la section, celle-ci sera ignorée ;</span><span class="sxs-lookup"><span data-stu-id="e01d3-p102">A default access entry that specifies the default read and write operations allowed on this connection. If there is no default access entry in the section, the section will be ignored.</span></span>

- <span data-ttu-id="e01d3-110">une nouvelle chaîne de connexion qui remplace la chaîne de connexion cliente.</span><span class="sxs-lookup"><span data-stu-id="e01d3-110">A new connection string that replaces the client connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="e01d3-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e01d3-111">Syntax</span></span>

<span data-ttu-id="e01d3-112">Une entrée d'accès par défaut a la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="e01d3-112">A default access entry is of the form:</span></span>

`Access=accessRight`

<span data-ttu-id="e01d3-113">Une entrée de chaîne de connexion de remplacement a la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="e01d3-113">A replacement connection string entry is of the form:</span></span>

`Connect=connectionString`

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e01d3-114">Partie</span><span class="sxs-lookup"><span data-stu-id="e01d3-114">Part</span></span></p></th>
<th><p><span data-ttu-id="e01d3-115">Description</span><span class="sxs-lookup"><span data-stu-id="e01d3-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e01d3-116"><strong>Connect</strong></span><span class="sxs-lookup"><span data-stu-id="e01d3-116"><strong>Connect</strong></span></span></p></td>
<td><p><span data-ttu-id="e01d3-117">Chaîne littérale qui indique qu'il s'agit d'une entrée de chaîne de connexion.</span><span class="sxs-lookup"><span data-stu-id="e01d3-117">A literal string that indicates this is a connection string entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e01d3-118"><strong><em>connectionString</em></strong></span><span class="sxs-lookup"><span data-stu-id="e01d3-118"><strong><em>connectionString</em></strong></span></span></p></td>
<td><p><span data-ttu-id="e01d3-119">Chaîne qui remplace toute la chaîne de connexion cliente.</span><span class="sxs-lookup"><span data-stu-id="e01d3-119">A string that replaces the whole client connection string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e01d3-120"><strong>Access</strong></span><span class="sxs-lookup"><span data-stu-id="e01d3-120"><strong>Access</strong></span></span></p></td>
<td><p><span data-ttu-id="e01d3-121">Chaîne littérale qui indique qu'il s'agit d'une entrée d'accès.</span><span class="sxs-lookup"><span data-stu-id="e01d3-121">A literal string that indicates this is an access entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e01d3-122"><strong><em>accessRight</em></strong></span><span class="sxs-lookup"><span data-stu-id="e01d3-122"><strong><em>accessRight</em></strong></span></span></p></td>
<td><p><span data-ttu-id="e01d3-123">Un des droits d'accès suivants :
</span><span class="sxs-lookup"><span data-stu-id="e01d3-123">One of the following access rights:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="e01d3-124"><strong>NoAccess</strong>  : l'utilisateur ne peut pas accéder à la source de données.</span><span class="sxs-lookup"><span data-stu-id="e01d3-124"><strong>NoAccess</strong> — User cannot access the data source.</span></span></p></li>
<li><p><span data-ttu-id="e01d3-125"><strong>ReadOnly</strong>  : l'utilisateur peut lire la source de données.</span><span class="sxs-lookup"><span data-stu-id="e01d3-125"><strong>ReadOnly</strong> — User can read the data source.</span></span></p></li>
<li><p><span data-ttu-id="e01d3-126"><strong>ReadWrite</strong>  : l'utilisateur peut lire la source de données ou écrire dans celle-ci.</span><span class="sxs-lookup"><span data-stu-id="e01d3-126"><strong>ReadWrite</strong> — User can read or write to the data source.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e01d3-127">Si vous voulez autoriser n’importe quelle connexion (dans et désactivant le comportement par défaut du gestionnaire), définissez l’entrée d’accès dans la section **connect default** et supprimer ou commentaire à n’importe quel autre section *d’identificateur de* **se connecter** .</span><span class="sxs-lookup"><span data-stu-id="e01d3-127">If you want to allow any connection (in effect, disabling the default handler behavior), set the access entry in the **connect default** section to , and delete or comment out any other **connect** *identifier* section.</span></span>

