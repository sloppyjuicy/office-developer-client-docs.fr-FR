---
title: CursorLocation, propriété (ADO)
TOCTitle: CursorLocation property (ADO)
ms:assetid: 8a048bd4-ae25-a555-1c07-14364b7e6560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249606(v=office.15)
ms:contentKeyID: 48546182
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25fd81acee3c541c8a3f315f96fa69241272a655
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295219"
---
# <a name="cursorlocation-property-ado"></a><span data-ttu-id="22062-102">CursorLocation, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="22062-102">CursorLocation property (ADO)</span></span>


<span data-ttu-id="22062-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="22062-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="22062-104">Indique l'emplacement du service de curseur.</span><span class="sxs-lookup"><span data-stu-id="22062-104">Indicates the location of the cursor service.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="22062-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="22062-105">Settings And Return Values</span></span>

<span data-ttu-id="22062-106">Définit ou renvoie une valeur de type **Long** qui peut être définie sur l’une des valeurs de [CursorLocationEnum](cursorlocationenum.md).</span><span class="sxs-lookup"><span data-stu-id="22062-106">Sets or returns a **Long** value that can be set to one of the [CursorLocationEnum](cursorlocationenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="22062-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="22062-107">Remarks</span></span>

<span data-ttu-id="22062-p101">Cette propriété permet de choisir l'une des différentes bibliothèques de curseurs accessibles au fournisseur. En général, vous pouvez choisir une bibliothèque de curseurs côté client ou une bibliothèque située sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="22062-p101">This property allows you to choose between various cursor libraries accessible to the provider. Usually, you can choose between using a client-side cursor library or one that is located on the server.</span></span>

<span data-ttu-id="22062-p102">Le paramètre de cette propriété n'affecte que les connexions établies après que la définition de la propriété. La modification de la propriété **CursorLocation** n'a aucun effet sur les connexions existantes.</span><span class="sxs-lookup"><span data-stu-id="22062-p102">This property setting affects connections established only after the property has been set. Changing the **CursorLocation** property has no effect on existing connections.</span></span>

<span data-ttu-id="22062-p103">Les curseurs renvoyés par la méthode [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) héritent de ce paramètre. Les objets **Recordset** héritent automatiquement ce paramètre de leurs connexions associées.</span><span class="sxs-lookup"><span data-stu-id="22062-p103">Cursors returned by the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) method inherit this setting. **Recordset** objects will automatically inherit this setting from their associated connections.</span></span>

<span data-ttu-id="22062-114">Cette propriété est en lecture/écriture dans un objet [Connection](connection-object-ado.md) ou un objet [Recordset](recordset-object-ado.md) fermé, et en lecture seule dans un objet **Recordset** ouvert.</span><span class="sxs-lookup"><span data-stu-id="22062-114">This property is read/write on a [Connection](connection-object-ado.md) or a closed [Recordset](recordset-object-ado.md), and read-only on an open **Recordset**.</span></span>

<span data-ttu-id="22062-115">**Utilisation du service de données à distance** Lorsqu’elle est utilisée sur un objet **Recordset** ou **Connection** côté client, la propriété **CursorLocation** ne peut être définie que **sur adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="22062-115">**Remote Data Service Usage** When used on a client-side **Recordset** or **Connection** object, the **CursorLocation** property can only be set to **adUseClient**.</span></span>

