---
title: AbsolutePage, propriété (ADO)
TOCTitle: AbsolutePage property (ADO)
ms:assetid: b6e5daac-cc21-0aa6-9119-a973595762bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249881(v=office.15)
ms:contentKeyID: 48547288
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: a285f9f9533e4ecd903e6cc6c0e427bf44c84ca4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870533"
---
# <a name="absolutepage-property-ado"></a><span data-ttu-id="3cb1a-102">AbsolutePage, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="3cb1a-102">AbsolutePage property (ADO)</span></span>

<span data-ttu-id="3cb1a-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3cb1a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3cb1a-104">Indique la page sur laquelle se trouve l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="3cb1a-104">Indicates on which page the current record resides.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="3cb1a-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="3cb1a-105">Settings and return values</span></span>

<span data-ttu-id="3cb1a-106">Définit ou renvoie une valeur de **type Long** comprise entre 1 et le nombre de pages dans l’objet [Recordset](recordset-object-ado.md) ([PageCount](pagecount-property-ado.md)) ou renvoie une des valeurs de [PositionEnum](positionenum.md) .</span><span class="sxs-lookup"><span data-stu-id="3cb1a-106">Sets or returns a **Long** value from 1 to the number of pages in the [Recordset](recordset-object-ado.md) object ([PageCount](pagecount-property-ado.md)), or returns one of the [PositionEnum](positionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cb1a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="3cb1a-107">Remarks</span></span>

<span data-ttu-id="3cb1a-p101">Cette propriété peut être utilisée pour identifier le numéro de page sur laquelle se trouve l'enregistrement actif. Elle utilise la propriété [PageSize](pagesize-property-ado.md) pour séparer logiquement le nombre total de jeux de lignes de l'objet **Recordset** en une série de pages, chacune possédant un nombre d'enregistrements égal à **PageSize** (à l'exception de la dernière page, qui peut comporter moins d'enregistrements). Le fournisseur doit prendre en charge les fonctions appropriées pour que cette propriété soit disponible.</span><span class="sxs-lookup"><span data-stu-id="3cb1a-p101">This property can be used to identify the page number on which the current record is located. It uses the [PageSize](pagesize-property-ado.md) property to logically divide the total rowset count of the **Recordset** object into a series of pages, each of which has the number of records equal to **PageSize** (except for the last page, which may have fewer records). The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="3cb1a-111">Lors de l'extraction ou de la définition de la propriété **AbsolutePage**, ADO utilise conjointement les propriétés [AbsolutePosition](absoluteposition-property-ado.md) et [PageSize](pagesize-property-ado.md), de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="3cb1a-111">When getting or setting the **AbsolutePage** property, ADO uses the [AbsolutePosition](absoluteposition-property-ado.md) property and the [PageSize](pagesize-property-ado.md) property together as follows:</span></span>

- <span data-ttu-id="3cb1a-112">Pour extraire **AbsolutePage**, ADO commence par extraire **AbsolutePosition**, qu'il divise par la valeur **PageSize**.</span><span class="sxs-lookup"><span data-stu-id="3cb1a-112">To get the **AbsolutePage**, ADO first retrieves the **AbsolutePosition**, and then divides it by the **PageSize**.</span></span>

- <span data-ttu-id="3cb1a-113">Pour définir **AbsolutePage**, ADO déplace **AbsolutePosition** de la manière suivante : il multiplie **PageSize** par la nouvelle valeur **AbsolutePage** et y ajoute 1.</span><span class="sxs-lookup"><span data-stu-id="3cb1a-113">To set the **AbsolutePage**, ADO moves the **AbsolutePosition** as follows: it multiplies the **PageSize** by the new **AbsolutePage** value and then adds 1 to the value.</span></span> <span data-ttu-id="3cb1a-114">Par conséquent, la position actuelle dans le **jeu d’enregistrements** une fois la valeur **AbsolutePage** est le premier enregistrement de cette page.</span><span class="sxs-lookup"><span data-stu-id="3cb1a-114">As a result, the current position in the **Recordset** after successfully setting **AbsolutePage** is the first record in that page.</span></span>

<span data-ttu-id="3cb1a-p103">Comme la propriété **AbsolutePosition**, la propriété **AbsolutePage** est en base 1 et est égale à 1 lorsque l'enregistrement actif correspond au premier enregistrement du **Recordset**. Définissez cette propriété pour accéder au premier enregistrement d'une page déterminée. Obtenez le nombre total de pages à partir de la propriété **PageCount**.</span><span class="sxs-lookup"><span data-stu-id="3cb1a-p103">Like the **AbsolutePosition** property, **AbsolutePage** is 1-based and equals 1 when the current record is the first record in the **Recordset**. Set this property to move to the first record of a particular page. Obtain the total number of pages from the **PageCount** property.</span></span>

