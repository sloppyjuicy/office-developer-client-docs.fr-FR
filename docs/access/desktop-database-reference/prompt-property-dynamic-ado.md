---
title: Prompt, propriété dynamique (ADO)
TOCTitle: Prompt dynamic property (ADO)
ms:assetid: 6c899b03-1d1f-a81f-dc17-7205a0230af9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249428(v=office.15)
ms:contentKeyID: 48545473
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 261ac5640b5239f27ad91e01d1cb23794f88740a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715185"
---
# <a name="prompt-dynamic-property-ado"></a>Prompt, propriété dynamique (ADO)

**S’applique à**: Access 2013, Office 2013

Spécifie si le fournisseur OLE DB doit inviter l'utilisateur à fournir des informations d'initialisation.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit et renvoie une valeur [ConnectPromptEnum](connectpromptenum.md).

## <a name="remarks"></a>Notes

**Prompt** est une propriété dynamique, qui peut être ajoutée à la collection [Properties](connection-object-ado.md) de l'objet [Connection](properties-collection-ado.md), par le fournisseur OLE DB. Pour inviter l'utilisateur à fournir les informations d'initialisation, les fournisseurs OLE DB affichent généralement une boîte de dialogue.

Les propriétés dynamiques d'un objet [Connection](connection-object-ado.md) sont perdues lorsque la **connexion** est fermée. Pour utiliser une valeur autre que la valeur par défaut, la propriété **Prompt** doit être réinitialisée avant de rouvrir l'objet **Connection**.

> [!NOTE]
> [!REMARQUE] Ne spécifiez pas que le fournisseur doit afficher une invite utilisateur dans les cas où l'utilisateur ne sera pas en mesure de répondre. Ainsi, l'utilisateur ne peut pas répondre si l'application est exécutée sur un système serveur et non sur le client de l'utilisateur, ou si l'application est exécutée sur un système auquel aucun utilisateur n'est connecté. En pareils cas, l'application attendra indéfiniment une réponse et semblera bloquée.

**Utilisation**

```vb
    Set cn = New Connection
    cn.Provider = "SQLOLEDB"
    cn.Properties("Prompt") = adPromptNever    ' do not prompt the user
```
