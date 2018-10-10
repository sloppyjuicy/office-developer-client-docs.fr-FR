---
title: Update Resync, propriété dynamique (ADO)
TOCTitle: Update Resync Property--Dynamic (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 16600f22084718a6b32656ebfc56d6a9be06c676
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470649"
---
# <a name="update-resync-property--dynamic-ado"></a>Update Resync, propriété dynamique (ADO)


**S’applique à**: Access 2013 | Office 2013

Spécifie si la méthode [UpdateBatch](updatebatch-method-ado.md) est suivie d'une opération de méthode [Resync](resync-method-ado.md) implicite et, si c'est le cas, la portée de cette opération.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une ou plusieurs de la [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) valeurs.

## <a name="remarks"></a>Remarques

Les valeurs de ADCPROP\_UPDATERESYNC\_ENUM peut-être être combinée, à l’exception d’adResyncAll qui représente déjà la combinaison des autres valeurs.

La constante **adResyncConflicts** stocke les valeurs de resynchronisation comme des valeurs sous-jacentes, mais ne remplace pas les modifications en attente.

La propriété **Update Resync** est une propriété dynamique ajoutée à la collection [Properties](recordset-object-ado.md) de l'objet [Recordset](properties-collection-ado.md) lorsque la propriété [CursorLocation](cursorlocation-property-ado.md) a la valeur **adUseClient**.

