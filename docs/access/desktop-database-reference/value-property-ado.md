---
title: Value, propriété (ADO)
TOCTitle: Value property (ADO)
ms:assetid: ff21d122-98e3-2b48-d92f-e696b8079fc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250310(v=office.15)
ms:contentKeyID: 48548958
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 00b82706d934356621ac1e41fffca61ec88e081f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715066"
---
# <a name="value-property-ado"></a>Value, propriété (ADO)

**S’applique à**: Access 2013, Office 2013

Indique la valeur attribuée à un objet [Field](field-object-ado.md), [Parameter](parameter-object-ado.md) ou [Property](property-object-ado.md).

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur **Variant** qui indique la valeur de l'objet. La valeur par défaut dépend de la propriété [Type](type-property-ado.md).

## <a name="remarks"></a>Remarques

Utilisez la propriété **Valeur** pour définir ou renvoyer des données d'objets **Field**, pour définir ou renvoyer des valeurs de paramètres avec les objets **Parameter** ou pour définir ou renvoyer des paramètres de propriété avec les objets **Property**. La propriété **Value** peut être en lecture/écriture ou en lecture seule ; cela dépend de nombreux facteurs (voir les rubriques sur les objets concernés pour plus d'informations).

ADO permet de définir et de renvoyer des données binaires longues avec la propriété **Value**.

> [!NOTE]
> [!REMARQUE] Pour les objets **Parameter**, ADO lit la propriété **Value** une seule fois à partir du fournisseur. Si une commande contient un objet **Parameter** dont la propriété **Value** est vide et que vous créez un [Recordset](recordset-object-ado.md) à partir de la commande, veillez à fermer le **Recordset** avant d'extraire la propriété **Value**. Sinon, pour certains fournisseurs, la propriété **Value** risque d'être vide ou de ne pas contenir la bonne valeur.

Pour les nouveaux objets **Field** ajoutés à la collection [Fields](fields-collection-ado.md) d'un objet [Record](record-object-ado.md), la propriété **Value** doit être définie avant les propriétés **Field**. Il faut d'abord attribuer une valeur spécifique à la propriété **Value** et appeler [Update](update-method-ado.md) sur la collection **Fields**. Il sera alors possible d'accéder aux autres propriétés comme [Type](type-property-ado.md) ou [Attributes](attributes-property-ado.md).

