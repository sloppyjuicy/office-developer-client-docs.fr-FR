---
title: Field, objet - ActiveX Data Objects (ADO)
TOCTitle: Field Object (ADO)
ms:assetid: 1dbd535e-48ad-a5c8-a1b2-6776c1e3e19d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248968(v=office.15)
ms:contentKeyID: 48543600
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 307d0770efc27a483e55e3d50b3a5bffeaff674c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883644"
---
# <a name="field-object-ado"></a>Field, objet (ADO)


**S’applique à**: Access 2013, Office 2013

Représente une colonne de données avec un type de données commun.

## <a name="remarks"></a>Notes

Chaque objet **Field** correspond à une colonne du [Recordset](recordset-object-ado.md). Vous utilisez la propriété [Value](value-property-ado.md) des objets **Field** pour définir ou renvoyer des données pour l'enregistrement actif. Selon les fonctionnalités proposées par le fournisseur, certaines collections, méthodes ou propriétés d'un objet **Field** risquent de ne pas être disponibles.

Les collections, les méthodes et les propriétés d'un objet **Field** vous permettent d'effectuer diverses tâches :

  - renvoyer le nom d'un champ avec la propriété [Name](name-property-ado.md) ;

  - afficher ou modifier les données d'un champ avec la propriété **Value** ( **Value** étant la propriété par défaut de l'objet **Field** ) ;

  - renvoyer les caractéristiques de base d'un champ à l'aide des propriétés [Type](type-property-ado.md), [Precision](precision-property-ado.md) et [NumericScale](numericscale-property-ado.md) ;

  - renvoyer la taille déclarée d'un champ avec la propriété [DefinedSize](definedsize-property-ado.md) ;

  - renvoyer la taille réelle des données d'un champ donné au moyen de la propriété [ActualSize](actualsize-property-ado.md) ;

  - déterminer quels types de fonctionnalités sont prises en charge pour un champ donné avec la propriété [Attributes](attributes-property-ado.md) et la collection [Properties](properties-collection-ado.md) ;

  - manipuler les valeurs de champs contenant des données binaires longues ou caractères longs avec les méthodes [AppendChunk](appendchunk-method-ado.md) et [GetChunk](getchunk-method-ado.md) ;

  - si le fournisseur prend en charge les mises à jour par lot, résoudre les incohérences présentes dans les valeurs des champs pendant la mise à jour par lot avec les propriétés [OriginalValue](originalvalue-property-ado.md) et [UnderlyingValue](underlyingvalue-property-ado.md).

Toutes les propriétés de métadonnées (**Name**, **Type**, **DefinedSize**, **Precision** et **NumericScale**) sont disponibles avant d'ouvrir le **Recordset** de l'objet **Field**. En les définissant à ce moment-là, vous facilitez la construction dynamique des formulaires.

