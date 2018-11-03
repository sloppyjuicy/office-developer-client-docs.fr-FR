---
title: GetChildren, méthode (ADO)
TOCTitle: GetChildren method (ADO)
ms:assetid: 998cf640-ffc7-51e1-4d1e-4797f7cdea4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249687(v=office.15)
ms:contentKeyID: 48546515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dcc687e5151e95d61939c30aa4c6be4063b67c47
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931266"
---
# <a name="getchildren-method-ado"></a><span data-ttu-id="fc4d8-102">GetChildren, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="fc4d8-102">GetChildren method (ADO)</span></span>


<span data-ttu-id="fc4d8-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc4d8-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="fc4d8-104">Retourne un objet [Recordset](recordset-object-ado.md) dont les lignes représentent les enfants d'un objet [Record](record-object-ado.md) d'une collection.</span><span class="sxs-lookup"><span data-stu-id="fc4d8-104">Returns a [Recordset](recordset-object-ado.md) whose rows represent the children of a collection [Record](record-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fc4d8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc4d8-105">Syntax</span></span>

<span data-ttu-id="fc4d8-106">**La valeur** *jeu d’enregistrements*  =  *enregistrement*. GetChildren</span><span class="sxs-lookup"><span data-stu-id="fc4d8-106">**Set** *recordset* = *record*.GetChildren</span></span>

## <a name="return-value"></a><span data-ttu-id="fc4d8-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fc4d8-107">Return value</span></span>

<span data-ttu-id="fc4d8-p101">Objet **Recordset** dont chaque ligne représente un enfant de l'objet **Record** actif. Par exemple, les enfants d'un objet **Record** qui représente un répertoire, sont les fichiers et sous-répertoires contenus dans le répertoire parent.</span><span class="sxs-lookup"><span data-stu-id="fc4d8-p101">A **Recordset** object for which each row represents a child of the current **Record** object. For example, the children of a **Record** that represents a directory would be the files and subdirectories contained within the parent directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc4d8-110">Notes</span><span class="sxs-lookup"><span data-stu-id="fc4d8-110">Remarks</span></span>

<span data-ttu-id="fc4d8-p102">Le fournisseur détermine les colonnes qui figureront dans l'objet **Recordset** retourné. Par exemple, un fournisseur de source de documents retourne toujours un objet **Recordset** de ressource.</span><span class="sxs-lookup"><span data-stu-id="fc4d8-p102">The provider determines what columns exist in the returned **Recordset**. For example, a document source provider always returns a resource **Recordset**.</span></span>

