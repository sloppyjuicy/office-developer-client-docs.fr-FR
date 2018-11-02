---
title: Méthode Database.NewPassword (DAO)
TOCTitle: NewPassword Method
ms:assetid: 01c1c454-d651-222c-225a-2b02734a1b7a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844754(v=office.15)
ms:contentKeyID: 48542941
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052943
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f4dca778da3c364d9e9b5a5eaf8ebbc32501853f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919359"
---
# <a name="databasenewpassword-method-dao"></a><span data-ttu-id="3ccbc-102">Méthode Database.NewPassword (DAO)</span><span class="sxs-lookup"><span data-stu-id="3ccbc-102">Database.NewPassword method (DAO)</span></span>


<span data-ttu-id="3ccbc-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3ccbc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3ccbc-104">Permet de modifier le mot de passe d'une base de données existante du moteur de base de données Microsoft Access (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="3ccbc-104">Changes the password of an existing Microsoft Access database engine database (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="3ccbc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ccbc-105">Syntax</span></span>

<span data-ttu-id="3ccbc-106">*expression* . NewPassword (***chaînes bstrAncien***, ***bstrNouveau***)</span><span class="sxs-lookup"><span data-stu-id="3ccbc-106">*expression* .NewPassword(***bstrOld***, ***bstrNew***)</span></span>

<span data-ttu-id="3ccbc-107">*expression* Expression qui renvoie un objet de **base de données** .</span><span class="sxs-lookup"><span data-stu-id="3ccbc-107">*expression* An expression that returns a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="3ccbc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3ccbc-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3ccbc-109">Name</span><span class="sxs-lookup"><span data-stu-id="3ccbc-109">Name</span></span></p></th>
<th><p><span data-ttu-id="3ccbc-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="3ccbc-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="3ccbc-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="3ccbc-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="3ccbc-112">Description</span><span class="sxs-lookup"><span data-stu-id="3ccbc-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ccbc-113">chaînes bstrAncien</span><span class="sxs-lookup"><span data-stu-id="3ccbc-113">bstrOld</span></span></p></td>
<td><p><span data-ttu-id="3ccbc-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3ccbc-114">Required</span></span></p></td>
<td><p><span data-ttu-id="3ccbc-115"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="3ccbc-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="3ccbc-116">Définition actuelle de la propriété <strong>Password</strong> de l'objet <strong>Database</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ccbc-116">The current setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ccbc-117">bstrNouveau</span><span class="sxs-lookup"><span data-stu-id="3ccbc-117">bstrNew</span></span></p></td>
<td><p><span data-ttu-id="3ccbc-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3ccbc-118">Required</span></span></p></td>
<td><p><span data-ttu-id="3ccbc-119"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="3ccbc-119"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="3ccbc-120">Le nouveau paramètre de la propriété de <strong>mot de passe</strong> de l’objet de <strong>base de données</strong> .</span><span class="sxs-lookup"><span data-stu-id="3ccbc-120">The new setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p>

> [!NOTE]
> <span data-ttu-id="3ccbc-p101">[!REMARQUE] Définissez des mots de passe forts qui combinent des lettres minuscules et majuscules, des nombres et des symboles. Les mots de passe faibles ne regroupent pas ces éléments. Mot de passe fort : Y6dh!et5. Mot de passe faible : Maison27. Utilisez un mot de passe fort dont vous pouvez vous souvenir sans devoir le noter.</span><span class="sxs-lookup"><span data-stu-id="3ccbc-p101">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span>


</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3ccbc-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="3ccbc-126">Remarks</span></span>

<span data-ttu-id="3ccbc-127">Les chaînes bstrAncien et bstrNouveau peuvent comporter jusqu'à 20 caractères et peut comprendre des caractères, à l’exception du caractère ASCII 0 (null).</span><span class="sxs-lookup"><span data-stu-id="3ccbc-127">The bstrOld and bstrNew strings can be up to 20 characters long and can include any characters except the ASCII character 0 (null).</span></span> <span data-ttu-id="3ccbc-128">Pour effacer le mot de passe, utilisez une chaîne de longueur nulle (" ») pour l’argument bstrNouveau.</span><span class="sxs-lookup"><span data-stu-id="3ccbc-128">To clear the password, use a zero-length string ("") for bstrNew.</span></span>

<span data-ttu-id="3ccbc-129">Les mots de passe respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="3ccbc-129">Passwords are case-sensitive.</span></span>

<span data-ttu-id="3ccbc-130">Si une base de données n'est associée à aucun mot de passe, le moteur de base de données Microsoft Access en crée un automatiquement en transmettant une chaîne vide ("") pour l'ancien mot de passe.</span><span class="sxs-lookup"><span data-stu-id="3ccbc-130">If a database has no password, the Microsoft Access database engine will automatically create one by passing a zero-length string ("") for the old password.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="3ccbc-131">[!IMPORTANTE] Si vous perdez votre mot de passe, vous ne pourrez plus jamais ouvrir la base de données.</span><span class="sxs-lookup"><span data-stu-id="3ccbc-131">If you lose your password, you can never open the database again.</span></span>


