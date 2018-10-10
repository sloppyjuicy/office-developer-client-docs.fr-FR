---
title: CursorLocation, propriété (ADO)
TOCTitle: CursorLocation Property (ADO)
ms:assetid: 8a048bd4-ae25-a555-1c07-14364b7e6560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249606(v=office.15)
ms:contentKeyID: 48546182
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9805b032a0e1a203d2a4057fb74757826a2a47b4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470885"
---
# <a name="cursorlocation-property-ado"></a><span data-ttu-id="97a5e-102">CursorLocation, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="97a5e-102">CursorLocation Property (ADO)</span></span>


<span data-ttu-id="97a5e-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="97a5e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="97a5e-104">Indique l'emplacement du service de curseur.</span><span class="sxs-lookup"><span data-stu-id="97a5e-104">Indicates the location of the cursor service.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="97a5e-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="97a5e-105">Settings And Return Values</span></span>

<span data-ttu-id="97a5e-106">Définit ou renvoie une valeur de type **Long** qui peut être définie sur l'une des valeurs de [CursorLocationEnum](cursorlocationenum.md).</span><span class="sxs-lookup"><span data-stu-id="97a5e-106">Sets or returns a **Long** value that can be set to one of the [CursorLocationEnum](cursorlocationenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="97a5e-107">Notes</span><span class="sxs-lookup"><span data-stu-id="97a5e-107">Remarks</span></span>

<span data-ttu-id="97a5e-p101">Cette propriété permet de choisir l'une des différentes bibliothèques de curseurs accessibles au fournisseur. En général, vous pouvez choisir une bibliothèque de curseurs côté client ou une bibliothèque située sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="97a5e-p101">This property allows you to choose between various cursor libraries accessible to the provider. Usually, you can choose between using a client-side cursor library or one that is located on the server.</span></span>

<span data-ttu-id="97a5e-p102">Le paramètre de cette propriété n'affecte que les connexions établies après que la définition de la propriété. La modification de la propriété **CursorLocation** n'a aucun effet sur les connexions existantes.</span><span class="sxs-lookup"><span data-stu-id="97a5e-p102">This property setting affects connections established only after the property has been set. Changing the **CursorLocation** property has no effect on existing connections.</span></span>

<span data-ttu-id="97a5e-p103">Les curseurs renvoyés par la méthode [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) héritent de ce paramètre. Les objets **Recordset** héritent automatiquement ce paramètre de leurs connexions associées.</span><span class="sxs-lookup"><span data-stu-id="97a5e-p103">Cursors returned by the [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) method inherit this setting. **Recordset** objects will automatically inherit this setting from their associated connections.</span></span>

<span data-ttu-id="97a5e-114">Cette propriété est en lecture/écriture dans un objet [Connection](connection-object-ado.md) ou un objet [Recordset](recordset-object-ado.md) fermé, et en lecture seule dans un objet **Recordset** ouvert.</span><span class="sxs-lookup"><span data-stu-id="97a5e-114">This property is read/write on a [Connection](connection-object-ado.md) or a closed [Recordset](recordset-object-ado.md), and read-only on an open **Recordset**.</span></span>

<span data-ttu-id="97a5e-115">**L’utilisation du Service de données à distance** Lorsqu’elle est utilisée sur un côté client **Recordset** ou un objet **Connection** , la propriété **CursorLocation** peut uniquement être définie **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="97a5e-115">**Remote Data Service Usage**When used on a client-side **Recordset** or **Connection** object, the **CursorLocation** property can only be set to **adUseClient**.</span></span>

