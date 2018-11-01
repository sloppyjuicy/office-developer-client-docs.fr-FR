---
title: AbsolutePosition, propriété (ADO)
TOCTitle: AbsolutePosition property (ADO)
ms:assetid: 500be001-9fa1-177b-f19d-acf003a0cdc2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15)
ms:contentKeyID: 48544787
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: a090630b5db741f761314f598fcc783dd124d1cf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881859"
---
# <a name="absoluteposition-property-ado"></a>AbsolutePosition, propriété (ADO)

**S’applique à**: Access 2013, Office 2013

Indique la position ordinale de l'enregistrement actif de l'objet [Recordset](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur de type **Long** comprise entre 1 et le nombre d’enregistrements dans l’objet **Recordset** ([RecordCount](recordcount-property-ado.md)), ou renvoie l’une des valeurs de [PositionEnum](positionenum.md).

## <a name="remarks"></a>Remarques

Pour définir la propriété **AbsolutePosition** , ADO exige que le fournisseur OLE DB que vous utilisez implémente l’interface IRowsetLocate.

L'accès à la propriété **AbsolutePosition** d'un objet **Recordset** ouvert avec un curseur dynamique ou avant uniquement génère une erreur **adErrFeatureNotAvailable**. Avec les autres types de curseur, la position correcte est retournée pour autant que le fournisseur prenne en charge l'interface IRowsetScroll. Si le fournisseur ne prend pas en charge l'interface *IRowsetScroll*, la propriété est définie sur **adPosUnknown**. Reportez-vous à la documentation pour déterminer si l'interface *IRowsetScroll* est prise en charge.

La propriété **AbsolutePosition** permet d'accéder à un enregistrement donné, en fonction de sa position ordinale dans l'objet **Recordset** ou de déterminer la position ordinale de l'enregistrement actif. Le fournisseur doit prendre en charge les fonctionnalités requises pour que cette propriété soit disponible.

Comme la propriété [AbsolutePage](absolutepage-property-ado.md), la propriété **AbsolutePosition** est en base 1 et est égale à 1 lorsque l'enregistrement actif est le premier enregistrement de l'objet **Recordset**. Vous pouvez obtenir le nombre total d'enregistrements dans l'objet **Recordset** à partir de la propriété [RecordCount](recordcount-property-ado.md).

Lorsque vous définissez la propriété **AbsolutePosition** , même s’il s’agit un enregistrement dans le cache actif, ADO recharge le cache avec un nouveau groupe d’enregistrements commençant par l’enregistrement que vous avez spécifié. La propriété [CacheSize](cachesize-property-ado.md) détermine, quant à elle, la taille de ce groupe.


> [!NOTE]
> [!REMARQUE] Vous ne pouvez pas utiliser la propriété **AbsolutePosition** en tant que numéro d'enregistrement de substitution. La position d'un enregistrement donné change lorsque vous supprimez un enregistrement précédent. Rien ne garantit qu'un enregistrement donné possédera la même valeur **AbsolutePosition** si l'objet **Recordset** est actualisé ou rouvert. Signets sont toujours recommandé de conserver et renvoyer une position donnée et sont le seul moyen de se positionner dans tous les types d’objets **Recordset** .


