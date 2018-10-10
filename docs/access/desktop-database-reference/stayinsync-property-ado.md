---
title: StayInSync, propriété (ADO)
TOCTitle: StayInSync Property (ADO)
ms:assetid: 02c95c10-4032-14e1-e506-f334a8787142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248792(v=office.15)
ms:contentKeyID: 48542966
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f492b2c3f58084be55eca4787cde486dab29ca67
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471029"
---
# <a name="stayinsync-property-ado"></a><span data-ttu-id="374fd-102">StayInSync, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="374fd-102">StayInSync Property (ADO)</span></span>


<span data-ttu-id="374fd-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="374fd-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="374fd-104">Indique, dans un objet [Recordset](recordset-object-ado.md) hiérarchique, si la référence aux enregistrements enfants sous-jacents (c'est-à-dire le *chapitre*) change lorsque la position de la ligne parente.</span><span class="sxs-lookup"><span data-stu-id="374fd-104">Indicates, in a hierarchical [Recordset](recordset-object-ado.md) object, whether the reference to the underlying child records (that is, the *chapter*) changes when the parent row position changes.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="374fd-105">Paramètres et valeurs renvoyées</span><span class="sxs-lookup"><span data-stu-id="374fd-105">Settings and Return Values</span></span>

<span data-ttu-id="374fd-p101">Définit ou renvoie une valeur de type **Boolean**. La valeur par défaut est **True**. Avec une valeur **True**, le chapitre est mis à jour lorsque l'objet **Recordset** parent change de position de ligne ; en cas de valeur **False**, le chapitre continue à faire référence aux données du chapitre précédent même si l'objet **Recordset** parent a changé de position de ligne.</span><span class="sxs-lookup"><span data-stu-id="374fd-p101">Sets or returns a **Boolean** value. The default value is **True**. If **True**, the chapter will be updated if the parent **Recordset** object changes row position; if **False**, the chapter will continue to refer to data in the previous chapter even though the parent **Recordset** object has changed row position.</span></span>

## <a name="remarks"></a><span data-ttu-id="374fd-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="374fd-109">Remarks</span></span>

<span data-ttu-id="374fd-p102">Cette propriété s'applique aux objets Recordset hiérarchiques, comme ceux pris en charge par [Microsoft Data Shaping Service pour OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) et doit être définie sur le **Recordset** parent avant que le **Recordset** ne soit extrait. Cette propriété simplifie la navigation dans les jeux d'enregistrements hiérarchiques.</span><span class="sxs-lookup"><span data-stu-id="374fd-p102">This property applies to hierarchical Recordsets, such as those supported by the [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), and must be set on the parent **Recordset** before the child **Recordset** is retrieved. This property simplifies navigating hierarchical recordsets.</span></span>

