---
title: Index.Clustered, propriété (DAO)
TOCTitle: Clustered Property
ms:assetid: dd0876a9-b7fe-c8c8-e675-5ed758ce5bd3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835375(v=office.15)
ms:contentKeyID: 48548149
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052930
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 060963dc47c933fee903cd9b220adb45c7f63df6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291851"
---
# <a name="indexclustered-property-dao"></a><span data-ttu-id="983bb-102">Index.Clustered, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="983bb-102">Index.Clustered property (DAO)</span></span>

<span data-ttu-id="983bb-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="983bb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="983bb-p101">Définit ou renvoie une valeur qui indique si un objet **Index** représente un index cluster pour une table (espaces de travail Microsoft Access uniquement). Valeur de type **Boolean** en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="983bb-p101">Sets or returns a value that indicates whether an **Index** object represents a clustered index for a table (Microsoft Access workspaces only). Read/write **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="983bb-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="983bb-106">Syntax</span></span>

<span data-ttu-id="983bb-107">*.* Clustered</span><span class="sxs-lookup"><span data-stu-id="983bb-107">*expression* .Clustered</span></span>

<span data-ttu-id="983bb-108">*expression* Expression qui renvoie un objet **Index.**</span><span class="sxs-lookup"><span data-stu-id="983bb-108">*expression* An expression that returns a **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="983bb-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="983bb-109">Remarks</span></span>

<span data-ttu-id="983bb-110">Le paramètre ou la valeur renvoyée est un type de données booléen qui correspond à **True** si l'objet **Index** représente un index cluster.</span><span class="sxs-lookup"><span data-stu-id="983bb-110">The setting or return value is a Boolean data type that is **True** if the **Index** object represents a clustered index.</span></span>

<span data-ttu-id="983bb-p102">Certains formats de base de données de bureau IISAM utilisent les index cluster. Un index cluster est constitué d'un ou plusieurs champs qui organisent ensemble tous les enregistrements d'une table dans un ordre prédéfini. Il permet d'accéder facilement aux enregistrements d'une table dans laquelle les valeurs d'index ne peuvent pas être uniques.</span><span class="sxs-lookup"><span data-stu-id="983bb-p102">Some IISAM desktop database formats use clustered indexes. A clustered index consists of one or more nonkey fields that, taken together, arrange all records in a table in a predefined order. A clustered index provides efficient access to records in a table in which the index values may not be unique.</span></span>

<span data-ttu-id="983bb-114">La propriété **Clustered** est en lecture/écriture pour un nouvel objet **Index** qui n'a pas encore été ajouté à une collection et en lecture seule pour un objet **Index** existant d'une collection **Indexes**.</span><span class="sxs-lookup"><span data-stu-id="983bb-114">The **Clustered** property is read/write for a new **Index** object not yet appended to a collection and read-only for an existing **Index** object in an **Indexes** collection.</span></span>

> [!NOTE]
> - <span data-ttu-id="983bb-115">Les bases de données du moteur de base de données Microsoft Access ignorent la propriété **Clustered** car ce moteur ne prend pas en charge les index cluster.</span><span class="sxs-lookup"><span data-stu-id="983bb-115">Microsoft Access database engine databases ignore the **Clustered** property because the Microsoft Access database engine doesn't support clustered indexes.</span></span>
> - <span data-ttu-id="983bb-116">Pour les sources de données ODBC, la **propriété Clustered** renvoie toujours **la valeur False**; Il ne détecte pas si la source de données ODBC possède un index en cluster.</span><span class="sxs-lookup"><span data-stu-id="983bb-116">For ODBC data sources, the **Clustered** property always returns **False**; it does not detect whether or not the ODBC data source has a clustered index.</span></span>


