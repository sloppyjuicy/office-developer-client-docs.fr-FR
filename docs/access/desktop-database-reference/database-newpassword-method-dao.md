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
ms.openlocfilehash: e72d879482c3ed69b262f2f4d0f07a4e11f8fa4c
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998937"
---
# <a name="databasenewpassword-method-dao"></a><span data-ttu-id="2d683-102">Méthode Database.NewPassword (DAO)</span><span class="sxs-lookup"><span data-stu-id="2d683-102">Database.NewPassword method (DAO)</span></span>

<span data-ttu-id="2d683-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d683-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2d683-104">Permet de modifier le mot de passe d'une base de données existante du moteur de base de données Microsoft Access (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="2d683-104">Changes the password of an existing Microsoft Access database engine database (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="2d683-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d683-105">Syntax</span></span>

<span data-ttu-id="2d683-106">*expression* . NewPassword (***chaînes bstrAncien***, ***bstrNouveau***)</span><span class="sxs-lookup"><span data-stu-id="2d683-106">*expression* .NewPassword(***bstrOld***, ***bstrNew***)</span></span>

<span data-ttu-id="2d683-107">*expression* Expression qui renvoie un objet de **base de données** .</span><span class="sxs-lookup"><span data-stu-id="2d683-107">*expression* An expression that returns a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="2d683-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d683-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2d683-109">Name</span><span class="sxs-lookup"><span data-stu-id="2d683-109">Name</span></span></p></th>
<th><p><span data-ttu-id="2d683-110">Requis/facultatif</span><span class="sxs-lookup"><span data-stu-id="2d683-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="2d683-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="2d683-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="2d683-112">Description</span><span class="sxs-lookup"><span data-stu-id="2d683-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d683-113"><em>chaînes bstrAncien</em></span><span class="sxs-lookup"><span data-stu-id="2d683-113"><em>bstrOld</em></span></span></p></td>
<td><p><span data-ttu-id="2d683-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="2d683-114">Required</span></span></p></td>
<td><p><span data-ttu-id="2d683-115"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="2d683-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="2d683-116">Définition actuelle de la propriété <strong>Password</strong> de l'objet <strong>Database</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d683-116">The current setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d683-117"><em>bstrNouveau</em></span><span class="sxs-lookup"><span data-stu-id="2d683-117"><em>bstrNew</em></span></span></p></td>
<td><p><span data-ttu-id="2d683-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="2d683-118">Required</span></span></p></td>
<td><p><span data-ttu-id="2d683-119"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="2d683-119"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="2d683-120">Le nouveau paramètre de la propriété de <strong>mot de passe</strong> de l’objet de <strong>base de données</strong> .</span><span class="sxs-lookup"><span data-stu-id="2d683-120">The new setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p>
<p><span data-ttu-id="2d683-121"><strong>Remarque</strong>: utilisez des mots de passe forts combinant des majuscules et minuscules, nombres et des symboles.</span><span class="sxs-lookup"><span data-stu-id="2d683-121"><strong>NOTE</strong>: Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="2d683-122">Les mots de passe faibles ne regroupent pas ces éléments.</span><span class="sxs-lookup"><span data-stu-id="2d683-122">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="2d683-123">Mot de passe fort : Y6dh!et5.</span><span class="sxs-lookup"><span data-stu-id="2d683-123">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="2d683-124">Mot de passe faible : Maison27.</span><span class="sxs-lookup"><span data-stu-id="2d683-124">Weak password: House27.</span></span> <span data-ttu-id="2d683-125">Utilisez un mot de passe fort dont vous pouvez vous souvenir sans devoir le noter.</span><span class="sxs-lookup"><span data-stu-id="2d683-125">Use a strong password that you can remember so that you don't have to write it down.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2d683-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="2d683-126">Remarks</span></span>

<span data-ttu-id="2d683-127">Les chaînes bstrAncien et bstrNouveau peuvent comporter jusqu'à 20 caractères et peut comprendre des caractères, à l’exception du caractère ASCII 0 (null).</span><span class="sxs-lookup"><span data-stu-id="2d683-127">The bstrOld and bstrNew strings can be up to 20 characters long and can include any characters except the ASCII character 0 (null).</span></span> <span data-ttu-id="2d683-128">Pour effacer le mot de passe, utilisez une chaîne de longueur nulle (" ») pour l’argument bstrNouveau.</span><span class="sxs-lookup"><span data-stu-id="2d683-128">To clear the password, use a zero-length string ("") for bstrNew.</span></span>

<span data-ttu-id="2d683-129">Les mots de passe respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="2d683-129">Passwords are case-sensitive.</span></span>

<span data-ttu-id="2d683-130">Si une base de données n'est associée à aucun mot de passe, le moteur de base de données Microsoft Access en crée un automatiquement en transmettant une chaîne vide ("") pour l'ancien mot de passe.</span><span class="sxs-lookup"><span data-stu-id="2d683-130">If a database has no password, the Microsoft Access database engine will automatically create one by passing a zero-length string ("") for the old password.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="2d683-131">[!IMPORTANTE] Si vous perdez votre mot de passe, vous ne pourrez plus jamais ouvrir la base de données.</span><span class="sxs-lookup"><span data-stu-id="2d683-131">If you lose your password, you can never open the database again.</span></span>


