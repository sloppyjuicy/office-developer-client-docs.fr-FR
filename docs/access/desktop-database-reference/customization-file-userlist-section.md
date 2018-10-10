---
title: Section UserList du fichier de personnalisation
TOCTitle: Customization File UserList Section
ms:assetid: b60ba3b0-37d4-bb59-d3cd-2ab44d178b8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249873(v=office.15)
ms:contentKeyID: 48547263
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a14060858ad5cd90b410319a515eb271b2b397ea
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471227"
---
# <a name="customization-file-userlist-section"></a><span data-ttu-id="bb916-102">Section UserList du fichier de personnalisation</span><span class="sxs-lookup"><span data-stu-id="bb916-102">Customization File UserList Section</span></span>


<span data-ttu-id="bb916-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bb916-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bb916-104">La section **userlist** se rapporte à la section **se connecter** avec le même paramètre *identificateur* de section.</span><span class="sxs-lookup"><span data-stu-id="bb916-104">The **userlist** section pertains to the **connect** section with the same section *identifier* parameter.</span></span>

<span data-ttu-id="bb916-105">Cette section peut contenir une *entrée d’accès utilisateur*, qui spécifie les droits d’accès pour l’utilisateur spécifié et remplace *valeur par défaut* *entrée d’accès* dans la section **connect** correspondante.</span><span class="sxs-lookup"><span data-stu-id="bb916-105">This section can contain a *user access entry*, which specifies access rights for the specified user and overrides the *default* *access entry* in the matching **connect** section.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb916-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb916-106">Syntax</span></span>

<span data-ttu-id="bb916-107">Une entrée d'accès utilisateur a la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="bb916-107">A user access entry is of the form:</span></span>

<span data-ttu-id="bb916-108">*userName \*\*\* =* accessRights \*\*\*</span><span class="sxs-lookup"><span data-stu-id="bb916-108">*userName\*\*\*=* accessRights\*\*\*</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bb916-109">Élément</span><span class="sxs-lookup"><span data-stu-id="bb916-109">Part</span></span></p></th>
<th><p><span data-ttu-id="bb916-110">Description</span><span class="sxs-lookup"><span data-stu-id="bb916-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb916-111"><em>userName</em></span><span class="sxs-lookup"><span data-stu-id="bb916-111"><em>userName</em></span></span></p></td>
<td><p><span data-ttu-id="bb916-p101"><em>Nom d'utilisateur</em> de la personne utilisant cette connexion. Les noms d'utilisateurs valides sont établis à l'aide de la boîte de dialogue du <strong>Gestionnaire des services</strong> IIS.</span><span class="sxs-lookup"><span data-stu-id="bb916-p101">The <em>user name</em> of the person employing this connection. Valid user names are established with the IIS <strong>Service Manager</strong> dialog.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb916-114"><strong><em>accessRights</em></strong></span><span class="sxs-lookup"><span data-stu-id="bb916-114"><strong><em>accessRights</em></strong></span></span></p></td>
<td><p><span data-ttu-id="bb916-115">Un des droits d'accès suivants :
</span><span class="sxs-lookup"><span data-stu-id="bb916-115">One of the following access rights:</span></span><br />
</p>
<ul>
<li><p><span data-ttu-id="bb916-116"><strong>NoAccess</strong>  : l'utilisateur ne peut pas accéder à la source de données.</span><span class="sxs-lookup"><span data-stu-id="bb916-116"><strong>NoAccess</strong> — User cannot access the data source.</span></span></p></li>
<li><p><span data-ttu-id="bb916-117"><strong>ReadOnly</strong>  : l'utilisateur peut lire la source de données.</span><span class="sxs-lookup"><span data-stu-id="bb916-117"><strong>ReadOnly</strong> — User can read the data source.</span></span></p></li>
<li><p><span data-ttu-id="bb916-118"><strong>ReadWrite</strong>  : l'utilisateur peut lire la source de données ou écrire dans celle-ci.</span><span class="sxs-lookup"><span data-stu-id="bb916-118"><strong>ReadWrite</strong> — User can read or write to the data source.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

