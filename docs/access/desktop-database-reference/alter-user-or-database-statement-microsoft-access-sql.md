---
title: ALTER USER ou DATABASE, instruction (Microsoft Access SQL)
TOCTitle: ALTER USER or DATABASE statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2514ca6403ce70acae9e344d610fbd7b9ba7d73b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297178"
---
# <a name="alter-user-or-database-statement-microsoft-access-sql"></a><span data-ttu-id="31263-102">ALTER USER ou DATABASE, instruction (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="31263-102">ALTER USER or DATABASE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="31263-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="31263-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="31263-104">Change le mot de passe d'un utilisateur ou d'une base de données existant.</span><span class="sxs-lookup"><span data-stu-id="31263-104">Changes the password for an existing user or for a database.</span></span>

## <a name="syntax"></a><span data-ttu-id="31263-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31263-105">Syntax</span></span>

<span data-ttu-id="31263-106">ALTER DATABASE PASSWORD *nouveaumotdepasse ancienmotdepasse*</span><span class="sxs-lookup"><span data-stu-id="31263-106">ALTER DATABASE PASSWORD *newpassword oldpassword*</span></span>

<span data-ttu-id="31263-107">ALTER USER *utilisateur* PASSWORD *nouveaumotdepasse ancienmotdepasse*</span><span class="sxs-lookup"><span data-stu-id="31263-107">ALTER USER *user* PASSWORD *newpassword oldpassword*</span></span>

<span data-ttu-id="31263-108">L'instruction ALTER USER ou DATABASE est composée des arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="31263-108">The ALTER USER or DATABASE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="31263-109">Élément</span><span class="sxs-lookup"><span data-stu-id="31263-109">Part</span></span></p></th>
<th><p><span data-ttu-id="31263-110">Description</span><span class="sxs-lookup"><span data-stu-id="31263-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31263-111"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="31263-111"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="31263-112">Nom de l'utilisateur à ajouter au fichier d'informations du groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="31263-112">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31263-113"><em>newpassword</em></span><span class="sxs-lookup"><span data-stu-id="31263-113"><em>newpassword</em></span></span></p></td>
<td><p><span data-ttu-id="31263-114">Nouveau mot de passe à associer au nom de l'<em>utilisateur</em> ou de la <em>base de données</em> spécifié.</span><span class="sxs-lookup"><span data-stu-id="31263-114">The new password to be associated with the specified <em>user</em> or <em>database</em> name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31263-115"><em>oldpassword</em></span><span class="sxs-lookup"><span data-stu-id="31263-115"><em>oldpassword</em></span></span></p></td>
<td><p><span data-ttu-id="31263-116">Mot de passe existant à associer au nom de l'<em>utilisateur</em> ou du <em>groupe</em> spécifié.</span><span class="sxs-lookup"><span data-stu-id="31263-116">The existing password to be associated with the specified <em>user</em> or <em>group</em> name.</span></span></p></td>
</tr>
</tbody>
</table>

