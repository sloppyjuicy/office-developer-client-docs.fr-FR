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
# <a name="absoluteposition-property-ado"></a><span data-ttu-id="ef755-102">AbsolutePosition, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="ef755-102">AbsolutePosition Property (ADO)</span></span>


<span data-ttu-id="ef755-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ef755-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ef755-104">Indique la position ordinale de l'enregistrement actif de l'objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ef755-104">Indicates the ordinal position of a [Recordset](recordset-object-ado.md) object's current record.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="ef755-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="ef755-105">Settings and Return Values</span></span>

<span data-ttu-id="ef755-106">Définit ou renvoie une valeur de type **Long** comprise entre 1 et le nombre d’enregistrements dans l’objet **Recordset** ([RecordCount](recordcount-property-ado.md)), ou renvoie l’une des valeurs de [PositionEnum](positionenum.md).</span><span class="sxs-lookup"><span data-stu-id="ef755-106">Sets or returns a **Long** value from 1 to the number of records in the **Recordset** object ([RecordCount](recordcount-property-ado.md)), or returns one of the [PositionEnum](positionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef755-107">Notes</span><span class="sxs-lookup"><span data-stu-id="ef755-107">Remarks</span></span>

<span data-ttu-id="ef755-108">Pour définir la propriété **AbsolutePosition** avec ADO, le fournisseur OLE DB utilisé doit implémenter l'interface IRowsetLocate.</span><span class="sxs-lookup"><span data-stu-id="ef755-108">In order to set the **AbsolutePosition** property, ADO requires that the OLE DB provider you are using implement the IRowsetLocate interface.</span></span>

<span data-ttu-id="ef755-p101">L'accès à la propriété **AbsolutePosition** d'un objet **Recordset** ouvert avec un curseur dynamique ou avant uniquement génère une erreur **adErrFeatureNotAvailable**. Avec les autres types de curseur, la position correcte est retournée pour autant que le fournisseur prenne en charge l'interface IRowsetScroll. Si le fournisseur ne prend pas en charge l'interface *IRowsetScroll*, la propriété est définie sur **adPosUnknown**. Reportez-vous à la documentation pour déterminer si l'interface *IRowsetScroll* est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ef755-p101">Accessing the **AbsolutePosition** property of a **Recordset** that was opened with either a forward-only or dynamic cursor raises the error **adErrFeatureNotAvailable**. With other cursor types, the correct position will be returned as long as the provider supports the IRowsetScroll interface. If the provider does not support the *IRowsetScroll* interface, the property is set to **adPosUnknown**. See the documentation for your provider to determine whether it supports *IRowsetScroll*.</span></span>

<span data-ttu-id="ef755-p102">La propriété **AbsolutePosition** permet d'accéder à un enregistrement donné, en fonction de sa position ordinale dans l'objet **Recordset** ou de déterminer la position ordinale de l'enregistrement actif. Le fournisseur doit prendre en charge les fonctionnalités requises pour que cette propriété soit disponible.</span><span class="sxs-lookup"><span data-stu-id="ef755-p102">Use the **AbsolutePosition** property to move to a record based on its ordinal position in the **Recordset** object, or to determine the ordinal position of the current record. The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="ef755-p103">Comme la propriété [AbsolutePage](absolutepage-property-ado.md), la propriété **AbsolutePosition** est en base 1 et est égale à 1 lorsque l'enregistrement actif est le premier enregistrement de l'objet **Recordset**. Vous pouvez obtenir le nombre total d'enregistrements dans l'objet **Recordset** à partir de la propriété [RecordCount](recordcount-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ef755-p103">Like the [AbsolutePage](absolutepage-property-ado.md) property, **AbsolutePosition** is 1-based and equals 1 when the current record is the first record in the **Recordset**. You can obtain the total number of records in the **Recordset** object from the [RecordCount](recordcount-property-ado.md) property.</span></span>

<span data-ttu-id="ef755-p104">Lorsque vous définissez la propriété **AbsolutePosition**, même pour un enregistrement présent dans le cache actif, ADO recharge le cache avec un nouveau groupe d'enregistrements en commençant par l'enregistrement que vous avez spécifié. La propriété [CacheSize](cachesize-property-ado.md) détermine la taille de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="ef755-p104">When you set the **AbsolutePosition** property, even if it is to a record in the current cache, ADO reloads the cache with a new group of records starting with the record you specified. The [CacheSize](cachesize-property-ado.md) property determines the size of this group.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ef755-p105">[!REMARQUE] Vous ne devez pas utiliser la propriété <STRONG>AbsolutePosition</STRONG> comme numéro d'enregistrement de substitution. La position d'un enregistrement donné change lorsque vous supprimez un enregistrement précédent. Rien ne garantit qu'un enregistrement donné possédera la même valeur <STRONG>AbsolutePosition</STRONG> si l'objet <STRONG>Recordset</STRONG> est actualisé ou rouvert. Les signets restent le meilleur moyen de conserver et renvoyer une position donnée puisqu'ils offrent la possibilité de se positionner dans tous les types d'objets <STRONG>Recordset</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="ef755-p105">You should not use the <STRONG>AbsolutePosition</STRONG> property as a surrogate record number. The position of a given record changes when you delete a preceding record. There is also no assurance that a given record will have the same <STRONG>AbsolutePosition</STRONG> if the <STRONG>Recordset</STRONG> object is requeried or reopened. Bookmarks are still the recommended way of retaining and returning to a given position and are the only way of positioning across all types of <STRONG>Recordset</STRONG> objects.</span></span></P>


