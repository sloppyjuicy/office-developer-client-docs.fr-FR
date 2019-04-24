---
title: Mettre à jour la propriété dynamique Resync (ADO)
TOCTitle: Update Resync dynamic property (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 653291ade258d602d7ec523dcac7e9fe51dd91fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308343"
---
# <a name="update-resync-dynamic-property-ado"></a>Mettre à jour la propriété dynamique Resync (ADO)


**S’applique à** : Access 2013, Office 2013

Spécifie si la méthode [UpdateBatch](updatebatch-method-ado.md) est suivie d'une opération de méthode [Resync](resync-method-ado.md) implicite et, si c'est le cas, la portée de cette opération.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une ou plusieurs des valeurs [d'\_énumération ADCPROP UPDATERESYNC\_](adcprop-updateresync-enum.md) .

## <a name="remarks"></a>Remarques

Les valeurs de l'\_énumération ADCPROP UPDATERESYNC\_peuvent être combinées, à l'exception de adResyncAll qui représente déjà la combinaison des autres valeurs.

La constante **adResyncConflicts** stocke les valeurs de resynchronisation comme des valeurs sous-jacentes, mais ne remplace pas les modifications en attente.

La propriété **Update Resync** est une propriété dynamique ajoutée à la collection [Properties](recordset-object-ado.md) de l'objet [Recordset](properties-collection-ado.md) lorsque la propriété [CursorLocation](cursorlocation-property-ado.md) a la valeur **adUseClient**.

