---
title: Database.NewPassword, méthode (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 20f09dbfba50526409472f7eb804ba2c47e4d1d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294854"
---
# <a name="databasenewpassword-method-dao"></a><span data-ttu-id="9365c-102">Database.NewPassword, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="9365c-102">Database.NewPassword method (DAO)</span></span>

<span data-ttu-id="9365c-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9365c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9365c-104">Permet de modifier le mot de passe d’une base de données existante du moteur de base de données Microsoft Access (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="9365c-104">Changes the password of an existing Microsoft Access database engine database (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="9365c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9365c-105">Syntax</span></span>

<span data-ttu-id="9365c-106">*.* NewPassword(***bstrOld***, ***bstrNew***)</span><span class="sxs-lookup"><span data-stu-id="9365c-106">*expression* .NewPassword(***bstrOld***, ***bstrNew***)</span></span>

<span data-ttu-id="9365c-107">*expression* Expression qui renvoie un objet **Database.**</span><span class="sxs-lookup"><span data-stu-id="9365c-107">*expression* An expression that returns a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="9365c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9365c-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9365c-109">Nom</span><span class="sxs-lookup"><span data-stu-id="9365c-109">Name</span></span></p></th>
<th><p><span data-ttu-id="9365c-110">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="9365c-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="9365c-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="9365c-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="9365c-112">Description</span><span class="sxs-lookup"><span data-stu-id="9365c-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9365c-113"><em>bstrOld</em></span><span class="sxs-lookup"><span data-stu-id="9365c-113"><em>bstrOld</em></span></span></p></td>
<td><p><span data-ttu-id="9365c-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9365c-114">Required</span></span></p></td>
<td><p><span data-ttu-id="9365c-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="9365c-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="9365c-116">Définition actuelle de la propriété <strong>Password</strong> de l'objet <strong>Database</strong>.</span><span class="sxs-lookup"><span data-stu-id="9365c-116">The current setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9365c-117"><em>bstrNew</em></span><span class="sxs-lookup"><span data-stu-id="9365c-117"><em>bstrNew</em></span></span></p></td>
<td><p><span data-ttu-id="9365c-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9365c-118">Required</span></span></p></td>
<td><p><span data-ttu-id="9365c-119"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="9365c-119"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="9365c-120">Nouveau paramètre de la propriété <strong>Password</strong> de l’objet <strong>Database.</strong></span><span class="sxs-lookup"><span data-stu-id="9365c-120">The new setting of the <strong>Password</strong> property of the <strong>Database</strong> object.</span></span></p>
<p><span data-ttu-id="9365c-121"><strong>REMARQUE</strong>: utilisez des mots de passe forts qui combinent des lettres majuscules et minuscules, des chiffres et des symboles.</span><span class="sxs-lookup"><span data-stu-id="9365c-121"><strong>NOTE</strong>: Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="9365c-122">Les mots de passe faibles ne regroupent pas ces éléments.</span><span class="sxs-lookup"><span data-stu-id="9365c-122">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="9365c-123">Mot de passe fort : Y6dh!et5.</span><span class="sxs-lookup"><span data-stu-id="9365c-123">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="9365c-124">Mot de passe faible : Maison27.</span><span class="sxs-lookup"><span data-stu-id="9365c-124">Weak password: House27.</span></span> <span data-ttu-id="9365c-125">Utilisez un mot de passe fort facile à mémoriser afin de ne pas avoir à le noter.</span><span class="sxs-lookup"><span data-stu-id="9365c-125">Use a strong password that you can remember so that you don't have to write it down.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9365c-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="9365c-126">Remarks</span></span>

<span data-ttu-id="9365c-127">Les chaînes bstrOld et bstrNew peuvent comporter jusqu’à 20 caractères et inclure n’importe quel caractère à l’exception du caractère ASCII 0 (null).</span><span class="sxs-lookup"><span data-stu-id="9365c-127">The bstrOld and bstrNew strings can be up to 20 characters long and can include any characters except the ASCII character 0 (null).</span></span> <span data-ttu-id="9365c-128">Pour effacer le mot de passe, utilisez une chaîne nulle («  ») pour bstrNew.</span><span class="sxs-lookup"><span data-stu-id="9365c-128">To clear the password, use a zero-length string ("") for bstrNew.</span></span>

<span data-ttu-id="9365c-129">Les mots de passe respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="9365c-129">Passwords are case-sensitive.</span></span>

<span data-ttu-id="9365c-130">Si une base de données n'est associée à aucun mot de passe, le moteur de base de données Microsoft Access en crée un automatiquement en transmettant une chaîne vide ("") pour l'ancien mot de passe.</span><span class="sxs-lookup"><span data-stu-id="9365c-130">If a database has no password, the Microsoft Access database engine will automatically create one by passing a zero-length string ("") for the old password.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="9365c-131">[!IMPORTANTE] Si vous perdez votre mot de passe, vous ne pourrez plus jamais ouvrir la base de données.</span><span class="sxs-lookup"><span data-stu-id="9365c-131">If you lose your password, you can never open the database again.</span></span>


