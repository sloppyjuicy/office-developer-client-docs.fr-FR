---
title: Update Resync dynamic property (ADO)
TOCTitle: Update Resync dynamic property (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5eed22559b0645cdae4498438fd6926136fb3303
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631649"
---
# <a name="update-resync-dynamic-property-ado"></a>Update Resync dynamic property (ADO)


**S’applique à** : Access 2013, Office 2013

Spécifie si la méthode [UpdateBatch](updatebatch-method-ado.md) est suivie d'une opération de méthode [Resync](resync-method-ado.md) implicite et, si c'est le cas, la portée de cette opération.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une ou plusieurs des valeurs [ADCPROP \_ UPDATERESYNC \_ ENUM.](adcprop-updateresync-enum.md)

## <a name="remarks"></a>Remarques

Les valeurs d’ADCPROP UPDATERESYNC ENUM peuvent être combinées, à l’exception d’adResyncAll qui représente déjà la combinaison du reste des \_ \_ valeurs.

La constante **adResyncConflicts** stocke les valeurs de resynchronisation comme des valeurs sous-jacentes, mais ne remplace pas les modifications en attente.

La propriété **Update Resync** est une propriété dynamique ajoutée à la collection [Properties](recordset-object-ado.md) de l'objet [Recordset](properties-collection-ado.md) lorsque la propriété [CursorLocation](cursorlocation-property-ado.md) a la valeur **adUseClient**.

