---
title: Section de connexion du fichier de personnalisation
TOCTitle: Customization File Connect section
ms:assetid: 037abfb4-798d-4b09-6133-356969aee95c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248802(v=office.15)
ms:contentKeyID: 48542985
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8652aa2c028350aab79cdf101cba189026b9a5ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295141"
---
# <a name="customization-file-connect-section"></a><span data-ttu-id="3cab9-102">Section de connexion du fichier de personnalisation</span><span class="sxs-lookup"><span data-stu-id="3cab9-102">Customization File Connect section</span></span>

<span data-ttu-id="3cab9-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3cab9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3cab9-p101">Le comportement par défaut du gestionnaire est de refuser toutes les connexions. La section **connect** indique les exceptions à ce comportement. Par exemple, si toutes les sections **connect** sont absentes ou vides, par défaut, aucune connexion ne peut être établie.</span><span class="sxs-lookup"><span data-stu-id="3cab9-p101">The default behavior of the handler is to deny all connections. The **connect** section specifies exceptions to that behavior. For example, if all the **connect** sections were absent or empty, then by default no connections could be made.</span></span>

<span data-ttu-id="3cab9-107">La section **connect** peut contenir :</span><span class="sxs-lookup"><span data-stu-id="3cab9-107">The **connect** section can contain:</span></span>

- <span data-ttu-id="3cab9-p102">une entrée d'accès par défaut qui spécifie les opérations de lecture et d'écriture autorisées par défaut sur cette connexion. Si aucune entrée d'accès par défaut n'existe dans la section, celle-ci sera ignorée ;</span><span class="sxs-lookup"><span data-stu-id="3cab9-p102">A default access entry that specifies the default read and write operations allowed on this connection. If there is no default access entry in the section, the section will be ignored.</span></span>

- <span data-ttu-id="3cab9-110">une nouvelle chaîne de connexion qui remplace la chaîne de connexion cliente.</span><span class="sxs-lookup"><span data-stu-id="3cab9-110">A new connection string that replaces the client connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cab9-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3cab9-111">Syntax</span></span>

<span data-ttu-id="3cab9-112">Une entrée d'accès par défaut a la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="3cab9-112">A default access entry is of the form:</span></span>

`Access=accessRight`

<span data-ttu-id="3cab9-113">Une entrée de chaîne de connexion de remplacement a la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="3cab9-113">A replacement connection string entry is of the form:</span></span>

`Connect=connectionString`

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3cab9-114">Élément</span><span class="sxs-lookup"><span data-stu-id="3cab9-114">Part</span></span></p></th>
<th><p><span data-ttu-id="3cab9-115">Description</span><span class="sxs-lookup"><span data-stu-id="3cab9-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3cab9-116"><strong>Connect</strong></span><span class="sxs-lookup"><span data-stu-id="3cab9-116"><strong>Connect</strong></span></span></p></td>
<td><p><span data-ttu-id="3cab9-117">Chaîne littérale qui indique qu'il s'agit d'une entrée de chaîne de connexion.</span><span class="sxs-lookup"><span data-stu-id="3cab9-117">A literal string that indicates this is a connection string entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cab9-118"><strong><em>ChaîneConnexion</em></strong></span><span class="sxs-lookup"><span data-stu-id="3cab9-118"><strong><em>connectionString</em></strong></span></span></p></td>
<td><p><span data-ttu-id="3cab9-119">Chaîne qui remplace toute la chaîne de connexion cliente.</span><span class="sxs-lookup"><span data-stu-id="3cab9-119">A string that replaces the whole client connection string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cab9-120"><strong>Access</strong></span><span class="sxs-lookup"><span data-stu-id="3cab9-120"><strong>Access</strong></span></span></p></td>
<td><p><span data-ttu-id="3cab9-121">Chaîne littérale qui indique qu'il s'agit d'une entrée d'accès.</span><span class="sxs-lookup"><span data-stu-id="3cab9-121">A literal string that indicates this is an access entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cab9-122"><strong><em>accessRight</em></strong></span><span class="sxs-lookup"><span data-stu-id="3cab9-122"><strong><em>accessRight</em></strong></span></span></p></td>
<td><p><span data-ttu-id="3cab9-123">Un des droits d'accès suivants :</span><span class="sxs-lookup"><span data-stu-id="3cab9-123">One of the following access rights:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="3cab9-124"><strong>NoAccess</strong>  : l'utilisateur ne peut pas accéder à la source de données.</span><span class="sxs-lookup"><span data-stu-id="3cab9-124"><strong>NoAccess</strong> — User cannot access the data source.</span></span></p></li>
<li><p><span data-ttu-id="3cab9-125"><strong>ReadOnly</strong>  : l'utilisateur peut lire la source de données.</span><span class="sxs-lookup"><span data-stu-id="3cab9-125"><strong>ReadOnly</strong> — User can read the data source.</span></span></p></li>
<li><p><span data-ttu-id="3cab9-126"><strong>ReadWrite</strong>  : l'utilisateur peut lire la source de données ou écrire dans celle-ci.</span><span class="sxs-lookup"><span data-stu-id="3cab9-126"><strong>ReadWrite</strong> — User can read or write to the data source.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3cab9-127">Si vous voulez autoriser n'importe quelle connexion (et désactivant le comportement par défaut du gestionnaire), définissez l'entrée d'accès dans la section **Connect default** sur et supprimez ou commentez toute autre section d' *identificateur* **Connect** .</span><span class="sxs-lookup"><span data-stu-id="3cab9-127">If you want to allow any connection (in effect, disabling the default handler behavior), set the access entry in the **connect default** section to , and delete or comment out any other **connect** *identifier* section.</span></span>

