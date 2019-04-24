---
title: Propriété dynamique prompt (ADO)
TOCTitle: Prompt dynamic property (ADO)
ms:assetid: 6c899b03-1d1f-a81f-dc17-7205a0230af9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249428(v=office.15)
ms:contentKeyID: 48545473
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 261ac5640b5239f27ad91e01d1cb23794f88740a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301322"
---
# <a name="prompt-dynamic-property-ado"></a><span data-ttu-id="e8070-102">Propriété dynamique prompt (ADO)</span><span class="sxs-lookup"><span data-stu-id="e8070-102">Prompt dynamic property (ADO)</span></span>

<span data-ttu-id="e8070-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8070-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e8070-104">Spécifie si le fournisseur OLE DB doit inviter l'utilisateur à fournir des informations d'initialisation.</span><span class="sxs-lookup"><span data-stu-id="e8070-104">Specifies whether the OLE DB provider should prompt the user for initialization information.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="e8070-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e8070-105">Settings and return values</span></span>

<span data-ttu-id="e8070-106">Définit et renvoie une valeur [ConnectPromptEnum](connectpromptenum.md).</span><span class="sxs-lookup"><span data-stu-id="e8070-106">Sets and returns a [ConnectPromptEnum](connectpromptenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8070-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="e8070-107">Remarks</span></span>

<span data-ttu-id="e8070-p101">**Prompt** est une propriété dynamique, qui peut être ajoutée à la collection [Properties](connection-object-ado.md) de l'objet [Connection](properties-collection-ado.md), par le fournisseur OLE DB. Pour inviter l'utilisateur à fournir les informations d'initialisation, les fournisseurs OLE DB affichent généralement une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e8070-p101">**Prompt** is a dynamic property, which may be appended to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection by the OLE DB provider. To prompt for initialization information, OLE DB providers will typically display a dialog box to the user.</span></span>

<span data-ttu-id="e8070-p102">Les propriétés dynamiques d'un objet [Connection](connection-object-ado.md) sont perdues lorsque la **connexion** est fermée. Pour utiliser une valeur autre que la valeur par défaut, la propriété **Prompt** doit être réinitialisée avant de rouvrir l'objet **Connection**.</span><span class="sxs-lookup"><span data-stu-id="e8070-p102">Dynamic properties of a [Connection](connection-object-ado.md) object are lost when the **Connection** is closed. The **Prompt** property must be reset before re-opening the **Connection** to use a value other than the default.</span></span>

> [!NOTE]
> <span data-ttu-id="e8070-p103">[!REMARQUE] Ne spécifiez pas que le fournisseur doit afficher une invite utilisateur dans les cas où l'utilisateur ne sera pas en mesure de répondre. Ainsi, l'utilisateur ne peut pas répondre si l'application est exécutée sur un système serveur et non sur le client de l'utilisateur, ou si l'application est exécutée sur un système auquel aucun utilisateur n'est connecté. En pareils cas, l'application attendra indéfiniment une réponse et semblera bloquée.</span><span class="sxs-lookup"><span data-stu-id="e8070-p103">Do not specify that the provider should prompt the user in scenarios in which the user will not be able to respond to the dialog box. For example, the user will not be able to respond if the application is running on a server system instead of on the user's client, or if the application is running on a system with no user logged on. In these cases, the application will wait indefinitely for a response and seem to lock up.</span></span>

<span data-ttu-id="e8070-115">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="e8070-115">**Usage**</span></span>

```vb
    Set cn = New Connection
    cn.Provider = "SQLOLEDB"
    cn.Properties("Prompt") = adPromptNever    ' do not prompt the user
```
