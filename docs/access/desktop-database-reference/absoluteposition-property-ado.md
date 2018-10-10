---
title: AbsolutePosition, propriété (ADO)
TOCTitle: AbsolutePosition Property (ADO)
ms:assetid: 500be001-9fa1-177b-f19d-acf003a0cdc2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15)
ms:contentKeyID: 48544787
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3258ffcab87b16e4931c9881a8e8d1cd2143262f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472026"
---
# <a name="absoluteposition-property-ado"></a>AbsolutePosition, propriété (ADO)


**S’applique à**: Access 2013 | Office 2013

Indique la position ordinale de l'enregistrement actif de l'objet [Recordset](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur de type **Long** comprise entre 1 et le nombre d’enregistrements dans l’objet **Recordset** ([RecordCount](recordcount-property-ado.md)), ou renvoie l’une des valeurs de [PositionEnum](positionenum.md).

## <a name="remarks"></a>Notes

Pour définir la propriété **AbsolutePosition** avec ADO, le fournisseur OLE DB utilisé doit implémenter l'interface IRowsetLocate.

L'accès à la propriété **AbsolutePosition** d'un objet **Recordset** ouvert avec un curseur dynamique ou avant uniquement génère une erreur **adErrFeatureNotAvailable**. Avec les autres types de curseur, la position correcte est retournée pour autant que le fournisseur prenne en charge l'interface IRowsetScroll. Si le fournisseur ne prend pas en charge l'interface *IRowsetScroll*, la propriété est définie sur **adPosUnknown**. Reportez-vous à la documentation pour déterminer si l'interface *IRowsetScroll* est prise en charge.

La propriété **AbsolutePosition** permet d'accéder à un enregistrement donné, en fonction de sa position ordinale dans l'objet **Recordset** ou de déterminer la position ordinale de l'enregistrement actif. Le fournisseur doit prendre en charge les fonctionnalités requises pour que cette propriété soit disponible.

Comme la propriété [AbsolutePage](absolutepage-property-ado.md), la propriété **AbsolutePosition** est en base 1 et est égale à 1 lorsque l'enregistrement actif est le premier enregistrement de l'objet **Recordset**. Vous pouvez obtenir le nombre total d'enregistrements dans l'objet **Recordset** à partir de la propriété [RecordCount](recordcount-property-ado.md).

Lorsque vous définissez la propriété **AbsolutePosition**, même pour un enregistrement présent dans le cache actif, ADO recharge le cache avec un nouveau groupe d'enregistrements en commençant par l'enregistrement que vous avez spécifié. La propriété [CacheSize](cachesize-property-ado.md) détermine la taille de ce groupe.


> [!NOTE]
> <P>[!REMARQUE] Vous ne devez pas utiliser la propriété <STRONG>AbsolutePosition</STRONG> comme numéro d'enregistrement de substitution. La position d'un enregistrement donné change lorsque vous supprimez un enregistrement précédent. Rien ne garantit qu'un enregistrement donné possédera la même valeur <STRONG>AbsolutePosition</STRONG> si l'objet <STRONG>Recordset</STRONG> est actualisé ou rouvert. Les signets restent le meilleur moyen de conserver et renvoyer une position donnée puisqu'ils offrent la possibilité de se positionner dans tous les types d'objets <STRONG>Recordset</STRONG>.</P>


