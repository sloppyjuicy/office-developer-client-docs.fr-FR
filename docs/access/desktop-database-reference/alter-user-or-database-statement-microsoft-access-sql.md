---
title: Instruction ALTER USER ou DATABASE (Microsoft Access SQL)
TOCTitle: ALTER USER or DATABASE statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: f0baf0faab717c35da0313d36e2ec1ac73528255
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879437"
---
# <a name="alter-user-or-database-statement-microsoft-access-sql"></a><span data-ttu-id="5aba7-102">Instruction ALTER USER ou DATABASE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="5aba7-102">ALTER USER or DATABASE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="5aba7-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5aba7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5aba7-104">Change le mot de passe d'un utilisateur ou d'une base de données existant.</span><span class="sxs-lookup"><span data-stu-id="5aba7-104">Changes the password for an existing user or for a database.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aba7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5aba7-105">Syntax</span></span>

<span data-ttu-id="5aba7-106">ALTER DATABASE PASSWORD *NouveauMotDePasse ancienmotdepasse*</span><span class="sxs-lookup"><span data-stu-id="5aba7-106">ALTER DATABASE PASSWORD *newpassword oldpassword*</span></span>

<span data-ttu-id="5aba7-107">ALTER USER *utilisateur* PASSWORD *NouveauMotDePasse ancienmotdepasse*</span><span class="sxs-lookup"><span data-stu-id="5aba7-107">ALTER USER *user* PASSWORD *newpassword oldpassword*</span></span>

<span data-ttu-id="5aba7-108">L'instruction ALTER USER ou DATABASE est composée des arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="5aba7-108">The ALTER USER or DATABASE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5aba7-109">Argument</span><span class="sxs-lookup"><span data-stu-id="5aba7-109">Part</span></span></p></th>
<th><p><span data-ttu-id="5aba7-110">Description</span><span class="sxs-lookup"><span data-stu-id="5aba7-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5aba7-111"><em>utilisateur</em></span><span class="sxs-lookup"><span data-stu-id="5aba7-111"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="5aba7-112">Nom de l'utilisateur à ajouter au fichier d'informations du groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="5aba7-112">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5aba7-113"><em>nouveaumotdepasse </em></span><span class="sxs-lookup"><span data-stu-id="5aba7-113"><em>newpassword</em></span></span></p></td>
<td><p><span data-ttu-id="5aba7-114">Nouveau mot de passe à associer au nom de l'<em>utilisateur</em> ou de la <em>base de données</em> spécifié.</span><span class="sxs-lookup"><span data-stu-id="5aba7-114">The new password to be associated with the specified <em>user</em> or <em>database</em> name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5aba7-115"><em>ancienmotdepasse</em></span><span class="sxs-lookup"><span data-stu-id="5aba7-115"><em>oldpassword</em></span></span></p></td>
<td><p><span data-ttu-id="5aba7-116">Mot de passe existant à associer au nom de l'<em>utilisateur</em> ou du <em>groupe</em> spécifié.</span><span class="sxs-lookup"><span data-stu-id="5aba7-116">The existing password to be associated with the specified <em>user</em> or <em>group</em> name.</span></span></p></td>
</tr>
</tbody>
</table>

