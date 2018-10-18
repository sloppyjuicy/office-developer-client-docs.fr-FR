---
title: Supports, méthode (ADO)
TOCTitle: Supports Method (ADO)
ms:assetid: 2b4062ce-44df-4e84-1ce9-d6618c10c2af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249059(v=office.15)
ms:contentKeyID: 48543924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ceeab22cda05738fdcec090acb5b4a2d6fc88a5b
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604259"
---
# <a name="supports-method-ado"></a><span data-ttu-id="16887-102">Supports, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="16887-102">Supports Method (ADO)</span></span>


<span data-ttu-id="16887-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="16887-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="16887-104">Détermine si un objet [Recordset](recordset-object-ado.md) spécifié prend en charge un type de fonctionnalité particulier.</span><span class="sxs-lookup"><span data-stu-id="16887-104">Determines whether a specified [Recordset](recordset-object-ado.md) object supports a particular type of functionality.</span></span>

## <a name="syntax"></a><span data-ttu-id="16887-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16887-105">Syntax</span></span>

<span data-ttu-id="16887-106">*Boolean* = *jeu d’enregistrements*. Prend en charge (*CursorOptions*)</span><span class="sxs-lookup"><span data-stu-id="16887-106">*boolean* = *recordset*.Supports (*CursorOptions*)</span></span>

<span data-ttu-id="16887-107"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="16887-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="16887-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="16887-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="16887-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="16887-109">Return value</span></span>
>>>>>>> <span data-ttu-id="16887-110">master</span><span class="sxs-lookup"><span data-stu-id="16887-110">master</span></span>

<span data-ttu-id="16887-111">Renvoie une valeur de **type Boolean** qui indique si toutes les fonctionnalités identifiées par l’argument *CursorOptions* sont prises en charge par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="16887-111">Returns a **Boolean** value that indicates whether all of the features identified by the *CursorOptions* argument are supported by the provider.</span></span>

## <a name="parameters"></a><span data-ttu-id="16887-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16887-112">Parameters</span></span>

  - <span data-ttu-id="16887-113">*CursorOptions*</span><span class="sxs-lookup"><span data-stu-id="16887-113">*CursorOptions*</span></span>

  - <span data-ttu-id="16887-114">Expression de type **Long** comportant une ou plusieurs valeurs [CursorOptionEnum](cursoroptionenum.md).</span><span class="sxs-lookup"><span data-stu-id="16887-114">A **Long** expression that consists of one or more [CursorOptionEnum](cursoroptionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="16887-115">Notes</span><span class="sxs-lookup"><span data-stu-id="16887-115">Remarks</span></span>

<span data-ttu-id="16887-p101">Utilisez la méthode **Supports** pour déterminer les types de fonctionnalités prises en charge par un objet **Recordset**. Si l'objet **Recordset** prend en charge les fonctionnalités dont les constantes correspondantes se trouvent dans *CursorOptions*, la méthode **Supports** retourne **True**. Sinon, elle renvoie **False**.</span><span class="sxs-lookup"><span data-stu-id="16887-p101">Use the **Supports** method to determine what types of functionality a **Recordset** object supports. If the **Recordset** object supports the features whose corresponding constants are in *CursorOptions*, the **Supports** method returns **True**. Otherwise, it returns **False**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="16887-p102">[!REMARQUE] Même si la méthode <STRONG>Supports</STRONG> peut retourner la valeur <STRONG>True</STRONG> pour une fonctionnalité déterminée, cela ne signifie pas pour autant que le fournisseur peut rendre la fonctionnalité disponible en toutes circonstances. La méthode <STRONG>Supports</STRONG> indique simplement si le fournisseur peut prendre en charge la fonctionnalité spécifiée, en partant du principe que certaines conditions sont remplies. Par exemple, la méthode <STRONG>Supports</STRONG> peut indiquer qu'un objet <STRONG>Recordset</STRONG> prend en charge les mises à jour même si le curseur est basé sur une jointure de plusieurs tables, dont certaines colonnes ne peuvent pas être mises à jour.</span><span class="sxs-lookup"><span data-stu-id="16887-p102">Although the <STRONG>Supports</STRONG> method may return <STRONG>True</STRONG> for a given functionality, it does not guarantee that the provider can make the feature available under all circumstances. The <STRONG>Supports</STRONG> method simply returns whether the provider can support the specified functionality, assuming certain conditions are met. For example, the <STRONG>Supports</STRONG> method may indicate that a <STRONG>Recordset</STRONG> object supports updates even though the cursor is based on a multiple table join, some columns of which are not updatable.</span></span></P>


