---
title: IEnumFBBlock
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fad9c0fd-b523-db98-ee0d-78aad5914ff2
ms.openlocfilehash: 2b37aa2000218acc0663ee8e2db12f01b93c0663
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317625"
---
# <a name="ienumfbblock"></a>IEnumFBBlock

Prend en charge l'accès et l'énumération des blocs de données de disponibilité d'un utilisateur dans un intervalle de temps.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Hérite de:  <br/> |[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Fourni par :  <br/> |Fournisseur de disponibilité  <br/> |
|Identificateur de l'interface:  <br/> |**IEnumFBBlock** <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[Next](ienumfbblock-next.md) <br/> |Obtient le prochain nombre spécifié de blocs de données de disponibilité dans une énumération.  <br/> |
|[Skip](ienumfbblock-skip.md) <br/> |Ignore un nombre spécifié de blocs de données de disponibilité.  <br/> |
|[Reset](ienumfbblock-reset.md) <br/> |Réinitialise l'énumérateur en définissant le curseur au début.  <br/> |
|[Clone](ienumfbblock-clone.md) <br/> |Crée une copie de l'énumérateur à l'aide de la même restriction temporelle, mais en définissant le curseur au début de l'énumérateur.  <br/> |
|[Restrict](ienumfbblock-restrict.md) <br/> |Limite l'énumération à une période spécifiée.  <br/> |
   
## <a name="remarks"></a>Remarques

Une énumération contient des blocs de données de disponibilité qui ne se chevauchent pas dans le temps. Lorsqu'il y a des éléments qui se chevauchent dans un calendrier, Outlook fusionne ces éléments pour créer des blocs de disponibilité qui ne se chevauchent pas dans l'énumération en fonction de cet ordre de priorité: absent (e) du bureau, occupé (e).
  
Un fournisseur de disponibilité obtient cette interface et l'énumération pour un intervalle de temps pour un utilisateur via [IFreeBusyData](ifreebusydata.md).
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de type disponible/occupé](about-the-free-busy-api.md)  
- [Constantes (API de disponibilité)](constants-free-busy-api.md)  
- [IFreeBusyData](ifreebusydata.md)

