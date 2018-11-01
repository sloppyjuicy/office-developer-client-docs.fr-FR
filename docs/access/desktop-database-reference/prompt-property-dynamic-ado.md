---
title: Prompt, propriété dynamique (ADO)
TOCTitle: Prompt Property--Dynamic (ADO)
ms:assetid: 6c899b03-1d1f-a81f-dc17-7205a0230af9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249428(v=office.15)
ms:contentKeyID: 48545473
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 491aea720995ec140ef3701a5ffdbdc5171c4a32
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868356"
---
# <a name="prompt-property--dynamic-ado"></a><span data-ttu-id="a74d9-102">Prompt, propriété dynamique (ADO)</span><span class="sxs-lookup"><span data-stu-id="a74d9-102">Prompt Property--Dynamic (ADO)</span></span>


<span data-ttu-id="a74d9-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a74d9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a74d9-104">Spécifie si le fournisseur OLE DB doit inviter l'utilisateur à fournir des informations d'initialisation.</span><span class="sxs-lookup"><span data-stu-id="a74d9-104">Specifies whether the OLE DB provider should prompt the user for initialization information.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="a74d9-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="a74d9-105">Settings and return values</span></span>

<span data-ttu-id="a74d9-106">Définit et renvoie une valeur [ConnectPromptEnum](connectpromptenum.md).</span><span class="sxs-lookup"><span data-stu-id="a74d9-106">Sets and returns a [ConnectPromptEnum](connectpromptenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a74d9-107">Notes</span><span class="sxs-lookup"><span data-stu-id="a74d9-107">Remarks</span></span>

<span data-ttu-id="a74d9-p101">**Prompt** est une propriété dynamique, qui peut être ajoutée à la collection [Properties](connection-object-ado.md) de l'objet [Connection](properties-collection-ado.md), par le fournisseur OLE DB. Pour inviter l'utilisateur à fournir les informations d'initialisation, les fournisseurs OLE DB affichent généralement une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="a74d9-p101">**Prompt** is a dynamic property, which may be appended to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection by the OLE DB provider. To prompt for initialization information, OLE DB providers will typically display a dialog box to the user.</span></span>

<span data-ttu-id="a74d9-p102">Les propriétés dynamiques d'un objet [Connection](connection-object-ado.md) sont perdues lorsque la **connexion** est fermée. Pour utiliser une valeur autre que la valeur par défaut, la propriété **Prompt** doit être réinitialisée avant de rouvrir l'objet **Connection**.</span><span class="sxs-lookup"><span data-stu-id="a74d9-p102">Dynamic properties of a [Connection](connection-object-ado.md) object are lost when the **Connection** is closed. The **Prompt** property must be reset before re-opening the **Connection** to use a value other than the default.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a74d9-p103">[!REMARQUE] Ne spécifiez pas que le fournisseur doit afficher une invite utilisateur dans les cas où l'utilisateur ne sera pas en mesure de répondre. Ainsi, l'utilisateur ne peut pas répondre si l'application est exécutée sur un système serveur et non sur le client de l'utilisateur, ou si l'application est exécutée sur un système auquel aucun utilisateur n'est connecté. En pareils cas, l'application attendra indéfiniment une réponse et semblera bloquée.</span><span class="sxs-lookup"><span data-stu-id="a74d9-p103">Do not specify that the provider should prompt the user in scenarios in which the user will not be able to respond to the dialog box. For example, the user will not be able to respond if the application is running on a server system instead of on the user's client, or if the application is running on a system with no user logged on. In these cases, the application will wait indefinitely for a response and seem to lock up.</span></span></P>



<span data-ttu-id="a74d9-115">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="a74d9-115">**Usage**</span></span>

```vb
    Set cn = New Connection
    cn.Provider = "SQLOLEDB"
    cn.Properties("Prompt") = adPromptNever    ' do not prompt the user
```
