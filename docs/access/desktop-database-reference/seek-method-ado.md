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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308791"
---
# <a name="seek-method-ado"></a><span data-ttu-id="56798-102">Seek, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="56798-102">Seek method (ADO)</span></span>

<span data-ttu-id="56798-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="56798-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="56798-104">Effectue une recherche dans l’index d’un objet [Recordset](recordset-object-ado.md) pour retrouver rapidement la ligne qui correspond aux valeurs spécifiées et faire de cette ligne la position de ligne active.</span><span class="sxs-lookup"><span data-stu-id="56798-104">Searches the index of a [Recordset](recordset-object-ado.md) to quickly locate the row that matches the specified values, and changes the current row position to that row.</span></span>

## <a name="syntax"></a><span data-ttu-id="56798-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56798-105">Syntax</span></span>

<span data-ttu-id="56798-106">*recordset*. Seek *KeyValues*, *SeekOption*</span><span class="sxs-lookup"><span data-stu-id="56798-106">*recordset*.Seek *KeyValues*, *SeekOption*</span></span>

## <a name="parameters"></a><span data-ttu-id="56798-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56798-107">Parameters</span></span>

|<span data-ttu-id="56798-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="56798-108">Parameter</span></span>|<span data-ttu-id="56798-109">Description</span><span class="sxs-lookup"><span data-stu-id="56798-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="56798-110">*KeyValues*</span><span class="sxs-lookup"><span data-stu-id="56798-110">*KeyValues*</span></span> |<span data-ttu-id="56798-p101">Tableau de valeurs de type **Variant**. Un index se compose d'une ou plusieurs colonnes et le tableau contient une valeur à comparer à chaque colonne correspondante.</span><span class="sxs-lookup"><span data-stu-id="56798-p101">An array of **Variant** values. An index consists of one or more columns and the array contains a value to compare against each corresponding column.</span></span>|
|<span data-ttu-id="56798-113">*SeekOption*</span><span class="sxs-lookup"><span data-stu-id="56798-113">*SeekOption*</span></span> |<span data-ttu-id="56798-114">Valeur [SeekEnum](seekenum.md) qui spécifie le type de comparaison à effectuer entre les colonnes de l’index et les *ValeursClés* correspondantes.</span><span class="sxs-lookup"><span data-stu-id="56798-114">A [SeekEnum](seekenum.md) value that specifies the type of comparison to be made between the columns of the index and the corresponding *KeyValues*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="56798-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="56798-115">Remarks</span></span>

<span data-ttu-id="56798-p102">Il est conseillé d’utiliser conjointement la méthode **Seek** avec la propriété [Index](index-property-ado.md) si le fournisseur sous-jacent prend les index en charge sur l’objet **Recordset**. La méthode [Supports](supports-method-ado.md)**(adSeek)** permet de déterminer si le fournisseur sous-jacent prend **Seek** en charge, et la méthode **Supports(adIndex)** de déterminer si les index sont pris en charge par le fournisseur. (Par exemple, le [fournisseur OLE DB pour Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) prend **Seek** et **Index** en charge.)</span><span class="sxs-lookup"><span data-stu-id="56798-p102">Use the **Seek** method in conjunction with the [Index](index-property-ado.md) property if the underlying provider supports indexes on the **Recordset** object. Use the [Supports](supports-method-ado.md)**(adSeek)** method to determine whether the underlying provider supports **Seek**, and the **Supports(adIndex)** method to determine whether the provider supports indexes. (For example, the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) supports **Seek** and **Index**.)</span></span>

<span data-ttu-id="56798-p103">Si la méthode **Seek** ne trouve pas la ligne recherchée, aucune erreur n'est générée et la ligne est positionnée à la fin du **Recordset**. Veillez à définir la propriété **Index** sur l'index souhaité avant d'exécuter cette méthode.</span><span class="sxs-lookup"><span data-stu-id="56798-p103">If **Seek** does not find the desired row, no error occurs, and the row is positioned at the end of the **Recordset**. Set the **Index** property to the desired index before executing this method.</span></span>

<span data-ttu-id="56798-p104">Cette méthode n'est prise en charge qu'avec les curseurs côté serveur. Seek n'est pas prise en charge lorsque la valeur de la propriété **CursorLocation** de l'objet [Recordset](cursorlocation-property-ado.md) est **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="56798-p104">This method is supported only with server-side cursors. Seek is not supported when the **Recordset** object's [CursorLocation](cursorlocation-property-ado.md) property value is **adUseClient**.</span></span>

<span data-ttu-id="56798-123">Vous ne pouvez employer cette méthode que dans le seul cas où l'objet **Recordset** a été ouvert avec une valeur [adCmdTableDirect](commandtypeenum.md) pour **CommandTypeEnum**.</span><span class="sxs-lookup"><span data-stu-id="56798-123">This method can only be used when the **Recordset** object has been opened with a [CommandTypeEnum](commandtypeenum.md) value of **adCmdTableDirect**.</span></span>

