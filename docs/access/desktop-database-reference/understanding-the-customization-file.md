---
title: Présentation du fichier de personnalisation
TOCTitle: Understanding the Customization File
ms:assetid: 98fd5ec1-d5bd-cdd2-5eb5-9a1682fbed79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249686(v=office.15)
ms:contentKeyID: 48546507
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b977fc4273068ac52efe8960761a9e28a6234e2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314069"
---
# <a name="understanding-the-customization-file"></a><span data-ttu-id="985e7-102">Présentation du fichier de personnalisation</span><span class="sxs-lookup"><span data-stu-id="985e7-102">Understanding the Customization File</span></span>


<span data-ttu-id="985e7-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="985e7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="985e7-104">Chaque en-tête de section du fichier de personnalisation se compose de crochets ( ) contenant **\[\]** un type et un paramètre.</span><span class="sxs-lookup"><span data-stu-id="985e7-104">Each section header in the customization file consists of square brackets (**\[\]**) containing a type and parameter.</span></span> <span data-ttu-id="985e7-105">Les quatre types de section sont signalés par les chaînes littérales **connect**, **sql**, **userlist** ou **logs**.</span><span class="sxs-lookup"><span data-stu-id="985e7-105">The four section types are indicated by the literal strings **connect**, **sql**, **userlist**, or **logs**.</span></span> <span data-ttu-id="985e7-106">Le paramètre est la chaîne littérale, la valeur par défaut, un identificateur spécifié par l'utilisateur ou rien.</span><span class="sxs-lookup"><span data-stu-id="985e7-106">The parameter is the literal string, the default, a user-specified identifier, or nothing.</span></span>

<span data-ttu-id="985e7-107">En conséquence, chaque section est marquée par l'un des en-têtes de section suivants :</span><span class="sxs-lookup"><span data-stu-id="985e7-107">Therefore, each section is marked with one of the following section headers:</span></span>

```text 
 
[ connect   default     ]
[ connect   identifier  ]
[ sql       default     ]
[ sql       identifier  ]
[ userlist  identifier  ]
[ logs                  ]
```

<span data-ttu-id="985e7-108">Les en-têtes de section comportent les parties suivantes.</span><span class="sxs-lookup"><span data-stu-id="985e7-108">The section headers have the following parts.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="985e7-109">Élément</span><span class="sxs-lookup"><span data-stu-id="985e7-109">Part</span></span></p></th>
<th><p><span data-ttu-id="985e7-110">Description</span><span class="sxs-lookup"><span data-stu-id="985e7-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="985e7-111"><strong>connect</strong></span><span class="sxs-lookup"><span data-stu-id="985e7-111"><strong>connect</strong></span></span></p></td>
<td><p><span data-ttu-id="985e7-112">Chaîne littérale qui modifie une chaîne de connexion.</span><span class="sxs-lookup"><span data-stu-id="985e7-112">A literal string that modifies a connection string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="985e7-113"><strong>sql</strong></span><span class="sxs-lookup"><span data-stu-id="985e7-113"><strong>sql</strong></span></span></p></td>
<td><p><span data-ttu-id="985e7-114">Chaîne littérale qui modifie une chaîne de commande.</span><span class="sxs-lookup"><span data-stu-id="985e7-114">A literal string that modifies a command string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="985e7-115"><strong>userlist</strong></span><span class="sxs-lookup"><span data-stu-id="985e7-115"><strong>userlist</strong></span></span></p></td>
<td><p><span data-ttu-id="985e7-116">Chaîne littérale qui modifie les droits d'accès d'un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="985e7-116">A literal string that modifies the access rights of a specific user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="985e7-117"><strong>logs</strong></span><span class="sxs-lookup"><span data-stu-id="985e7-117"><strong>logs</strong></span></span></p></td>
<td><p><span data-ttu-id="985e7-118">Chaîne littérale qui spécifie un fichier journal dans lequel les erreurs liées aux opérations sont consignées.</span><span class="sxs-lookup"><span data-stu-id="985e7-118">A literal string that specifies a log file recording operational errors.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="985e7-119"><strong>default</strong></span><span class="sxs-lookup"><span data-stu-id="985e7-119"><strong>default</strong></span></span></p></td>
<td><p><span data-ttu-id="985e7-120">Chaîne littérale utilisée si aucun identificateur n'a été spécifié ou trouvé.</span><span class="sxs-lookup"><span data-stu-id="985e7-120">A literal string that is used if no identifier is specified or found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="985e7-121"><em>identificateur</em></span><span class="sxs-lookup"><span data-stu-id="985e7-121"><em>identifier</em></span></span></p></td>
<td><p><span data-ttu-id="985e7-122">Chaîne qui correspond à une chaîne de la chaîne <strong>connect</strong> ou <strong>command</strong>.</span><span class="sxs-lookup"><span data-stu-id="985e7-122">A string that matches a string in the <strong>connect</strong> or <strong>command</strong> string.</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="985e7-123">Utilisez cette section si l'en-tête de section contient la chaîne <strong>connect</strong> et si la chaîne de l'identificateur figure dans la chaîne de connexion.</span><span class="sxs-lookup"><span data-stu-id="985e7-123">Use this section if the section header contains <strong>connect</strong> and the identifier string is found in the connection string.</span></span></p></li>
<li><p><span data-ttu-id="985e7-124">Utilisez cette section si l'en-tête de section contient la chaîne <strong>sql</strong> et si la chaîne de l'identificateur figure dans la chaîne de connexion.</span><span class="sxs-lookup"><span data-stu-id="985e7-124">Use this section if the section header contains <strong>sql</strong> and the identifier string is found in the command string.</span></span></p></li>
<li><p><span data-ttu-id="985e7-125">Utilisez cette section si l'en-tête de section contient la chaîne <strong>userlist</strong> et si la chaîne de l'identificateur correspond à un identificateur de section <strong>connect</strong>.</span><span class="sxs-lookup"><span data-stu-id="985e7-125">Use this section if the section header contains <strong>userlist</strong> and the identifier string matches a <strong>connect</strong> section identifier.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="985e7-p102">L'objet **DataFactory** appelle le gestionnaire et lui passe les paramètres clients. Le gestionnaire recherche les chaînes entières dans les paramètres clients qui correspondent aux identificateurs des en-têtes de section appropriés. Si la recherche est infructueuse, le contenu de cette section est appliqué aux paramètres clients.</span><span class="sxs-lookup"><span data-stu-id="985e7-p102">The **DataFactory** calls the handler, passing client parameters. The handler searches for whole strings in the client parameters that match identifiers in the appropriate section headers. If a match is found, the contents of that section are applied to the client parameter.</span></span>

<span data-ttu-id="985e7-129">Une section spécifique est utilisée dans les circonstances suivantes :</span><span class="sxs-lookup"><span data-stu-id="985e7-129">A particular section is used under the following circumstances:</span></span>

  - <span data-ttu-id="985e7-130">Une section **de** connexion est utilisée si la partie valeur du mot clé de chaîne de connexion du client, « \**Data Source=\*\*\*value*», correspond à un identificateur de section **de** *connexion.*</span><span class="sxs-lookup"><span data-stu-id="985e7-130">A **connect** section is used if the value part of the client connect string keyword, "\**Data Source=\*\*\*value*", matches a **connect** section identifier *.*</span></span>

  - <span data-ttu-id="985e7-131">Une section **sql** est utilisée si la chaîne de commande cliente contient une chaîne qui correspond à un identificateur de section **sql**.</span><span class="sxs-lookup"><span data-stu-id="985e7-131">An **sql** section is used if the client command string contains a string that matches an **sql** section identifier.</span></span>

  - <span data-ttu-id="985e7-132">Une section **connect** ou **sql** avec un paramètre par défaut est utilisée en l'absence d'identificateur correspondant.</span><span class="sxs-lookup"><span data-stu-id="985e7-132">A **connect** or **sql** section with a default parameter is used if there is no matching identifier.</span></span>

  - <span data-ttu-id="985e7-p103">Une section **userlist** est utilisée si l'identificateur de section **userlist** correspond à un identificateur de section **connect**. Si c'est le cas, le contenu de la section **userlist** est appliqué à la connexion régie par la section **connect**.</span><span class="sxs-lookup"><span data-stu-id="985e7-p103">A **userlist** section is used if the **userlist** section identifier matches a **connect** section identifier. If there is a match, the contents of the **userlist** section are applied to the connection governed by the **connect** section.</span></span>

  - <span data-ttu-id="985e7-135">Si la chaîne de connexion ou de commande ne correspond pas à l'identificateur d'un en-tête de section **connect** ou **sql** et en l'absence d'un en-tête de section **connect** ou **sql** doté d'un paramètre par défaut, la chaîne cliente est utilisée telle quelle.</span><span class="sxs-lookup"><span data-stu-id="985e7-135">If the string in a connection or command string does not match the identifier in any **connect** or **sql** section header, and there is no **connect** or **sql** section header with a default parameter, then the client string is used without modification.</span></span>

  - <span data-ttu-id="985e7-136">La section **logs** est utilisée chaque fois que l'objet **DataFactory** est utilisé.</span><span class="sxs-lookup"><span data-stu-id="985e7-136">The **logs** section is used whenever the **DataFactory** is in operation.</span></span>

