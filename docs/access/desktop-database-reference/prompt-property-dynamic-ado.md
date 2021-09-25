---
title: Prompt dynamic, propriété (ADO)
TOCTitle: Prompt dynamic property (ADO)
ms:assetid: 6c899b03-1d1f-a81f-dc17-7205a0230af9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249428(v=office.15)
ms:contentKeyID: 48545473
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 60a6f6e8ea728466648249d9851b1ee326efed74
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577072"
---
# <a name="prompt-dynamic-property-ado"></a>Prompt dynamic, propriété (ADO)

**S’applique à** : Access 2013, Office 2013

Spécifie si le fournisseur OLE DB doit inviter l'utilisateur à fournir des informations d'initialisation.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit et renvoie une valeur [ConnectPromptEnum](connectpromptenum.md).

## <a name="remarks"></a>Remarques

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
