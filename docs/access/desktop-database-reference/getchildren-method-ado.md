---
title: GetChildren, méthode (ADO)
TOCTitle: GetChildren Method (ADO)
ms:assetid: 998cf640-ffc7-51e1-4d1e-4797f7cdea4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249687(v=office.15)
ms:contentKeyID: 48546515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a11f3e34f8dcb45bab88d8ff87e69067103e4640
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469610"
---
# <a name="getchildren-method-ado"></a><span data-ttu-id="8f015-102">GetChildren, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="8f015-102">GetChildren Method (ADO)</span></span>


<span data-ttu-id="8f015-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8f015-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="8f015-104">Retourne un objet [Recordset](recordset-object-ado.md) dont les lignes représentent les enfants d'un objet [Record](record-object-ado.md) d'une collection.</span><span class="sxs-lookup"><span data-stu-id="8f015-104">Returns a [Recordset](recordset-object-ado.md) whose rows represent the children of a collection [Record](record-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8f015-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f015-105">Syntax</span></span>

<span data-ttu-id="8f015-106">**La valeur** *jeu d’enregistrements*  =  *enregistrement*. GetChildren</span><span class="sxs-lookup"><span data-stu-id="8f015-106">**Set** *recordset* = *record*.GetChildren</span></span>

## <a name="return-value"></a><span data-ttu-id="8f015-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8f015-107">Return Value</span></span>

<span data-ttu-id="8f015-p101">Objet **Recordset** dont chaque ligne représente un enfant de l'objet **Record** actif. Par exemple, les enfants d'un objet **Record** qui représente un répertoire, sont les fichiers et sous-répertoires contenus dans le répertoire parent.</span><span class="sxs-lookup"><span data-stu-id="8f015-p101">A **Recordset** object for which each row represents a child of the current **Record** object. For example, the children of a **Record** that represents a directory would be the files and subdirectories contained within the parent directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f015-110">Notes</span><span class="sxs-lookup"><span data-stu-id="8f015-110">Remarks</span></span>

<span data-ttu-id="8f015-p102">Le fournisseur détermine les colonnes qui figureront dans l'objet **Recordset** retourné. Par exemple, un fournisseur de source de documents retourne toujours un objet **Recordset** de ressource.</span><span class="sxs-lookup"><span data-stu-id="8f015-p102">The provider determines what columns exist in the returned **Recordset**. For example, a document source provider always returns a resource **Recordset**.</span></span>

