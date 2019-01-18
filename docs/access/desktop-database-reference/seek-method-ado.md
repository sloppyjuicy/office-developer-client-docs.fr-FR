---
title: Seek, méthode - ActiveX Data Objects (ADO)
TOCTitle: Seek method (ADO)
ms:assetid: cf0f133b-31f2-a2df-6cf3-1b5fa73b516c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250027(v=office.15)
ms:contentKeyID: 48547802
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 321040a39b02f31f0265df6e91748df13c05032c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726301"
---
# <a name="seek-method-ado"></a><span data-ttu-id="e09f7-102">Seek, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="e09f7-102">Seek method (ADO)</span></span>

<span data-ttu-id="e09f7-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e09f7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e09f7-104">Effectue une recherche dans l'index d'un objet [Recordset](recordset-object-ado.md) pour retrouver rapidement la ligne qui correspond aux valeurs spécifiées et faire de cette ligne la position de ligne active.</span><span class="sxs-lookup"><span data-stu-id="e09f7-104">Searches the index of a [Recordset](recordset-object-ado.md) to quickly locate the row that matches the specified values, and changes the current row position to that row.</span></span>

## <a name="syntax"></a><span data-ttu-id="e09f7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e09f7-105">Syntax</span></span>

<span data-ttu-id="e09f7-106">*jeu d’enregistrements*. Seek*KeyValues*, *SeekOption*</span><span class="sxs-lookup"><span data-stu-id="e09f7-106">*recordset*.Seek*KeyValues*, *SeekOption*</span></span>

## <a name="parameters"></a><span data-ttu-id="e09f7-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="e09f7-107">Parameters</span></span>

|<span data-ttu-id="e09f7-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="e09f7-108">Parameter</span></span>|<span data-ttu-id="e09f7-109">Description</span><span class="sxs-lookup"><span data-stu-id="e09f7-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="e09f7-110">*KeyValues*</span><span class="sxs-lookup"><span data-stu-id="e09f7-110">*KeyValues*</span></span> |<span data-ttu-id="e09f7-p101">Tableau de valeurs de type **Variant**. Un index se compose d'une ou plusieurs colonnes et le tableau contient une valeur à comparer à chaque colonne correspondante.</span><span class="sxs-lookup"><span data-stu-id="e09f7-p101">An array of **Variant** values. An index consists of one or more columns and the array contains a value to compare against each corresponding column.</span></span>|
|<span data-ttu-id="e09f7-113">*SeekOption*</span><span class="sxs-lookup"><span data-stu-id="e09f7-113">*SeekOption*</span></span> |<span data-ttu-id="e09f7-114">Valeur [SeekEnum](seekenum.md) qui spécifie le type de comparaison à effectuer entre les colonnes de l’index et les *ValeursClés* correspondantes.</span><span class="sxs-lookup"><span data-stu-id="e09f7-114">A [SeekEnum](seekenum.md) value that specifies the type of comparison to be made between the columns of the index and the corresponding *KeyValues*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="e09f7-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e09f7-115">Remarks</span></span>

<span data-ttu-id="e09f7-116">Il est conseillé d'utiliser conjointement la méthode **Seek** avec la propriété [Index](index-property-ado.md) si le fournisseur sous-jacent prend en charge les index sur l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="e09f7-116">Use the **Seek** method in conjunction with the [Index](index-property-ado.md) property if the underlying provider supports indexes on the **Recordset** object.</span></span> <span data-ttu-id="e09f7-117">Utilisez la méthode **(adSeek)** [prend en charge](supports-method-ado.md)pour déterminer si le fournisseur sous-jacent prend en charge la **méthode Seek**et la méthode **supports (adIndex)** pour déterminer si le fournisseur prend en charge les index.</span><span class="sxs-lookup"><span data-stu-id="e09f7-117">Use the [Supports](supports-method-ado.md)**(adSeek)** method to determine whether the underlying provider supports **Seek**, and the **Supports(adIndex)** method to determine whether the provider supports indexes.</span></span> <span data-ttu-id="e09f7-118">(Par exemple, le [fournisseur OLE DB pour Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) prend **Seek** et **Index** en charge.)</span><span class="sxs-lookup"><span data-stu-id="e09f7-118">(For example, the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) supports **Seek** and **Index**.)</span></span>

<span data-ttu-id="e09f7-p103">Si la méthode **Seek** ne trouve pas la ligne recherchée, aucune erreur n'est générée et la ligne est positionnée à la fin du **Recordset**. Veillez à définir la propriété **Index** sur l'index souhaité avant d'exécuter cette méthode.</span><span class="sxs-lookup"><span data-stu-id="e09f7-p103">If **Seek** does not find the desired row, no error occurs, and the row is positioned at the end of the **Recordset**. Set the **Index** property to the desired index before executing this method.</span></span>

<span data-ttu-id="e09f7-p104">Cette méthode n'est prise en charge qu'avec les curseurs côté serveur. Seek n'est pas prise en charge lorsque la valeur de la propriété **CursorLocation** de l'objet [Recordset](cursorlocation-property-ado.md) est **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="e09f7-p104">This method is supported only with server-side cursors. Seek is not supported when the **Recordset** object's [CursorLocation](cursorlocation-property-ado.md) property value is **adUseClient**.</span></span>

<span data-ttu-id="e09f7-123">Vous ne pouvez employer cette méthode que dans le seul cas où l'objet **Recordset** a été ouvert avec une valeur [adCmdTableDirect](commandtypeenum.md) pour **CommandTypeEnum**.</span><span class="sxs-lookup"><span data-stu-id="e09f7-123">This method can only be used when the **Recordset** object has been opened with a [CommandTypeEnum](commandtypeenum.md) value of **adCmdTableDirect**.</span></span>

