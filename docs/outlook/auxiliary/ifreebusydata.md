---
title: IFreeBusyData
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c9a80ad3-6311-fe07-b6f7-9fd63424753b
ms.openlocfilehash: cd9d4dffd83e1995319b0f0d661435fedb78f28c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317498"
---
# <a name="ifreebusydata"></a>IFreeBusyData

Pour un utilisateur donné, obtient et définit une plage horaire et renvoie une interface pour l'énumération des blocs de données de disponibilité dans cette plage de temps.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Hérite de:  <br/> |[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Fourni par :  <br/> |Fournisseur de disponibilité  <br/> |
|Identificateur de l'interface:  <br/> |IID_IFreeBusyData  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[Placeholder1](ifreebusydata-placeholder1.md) <br/> | *Ce membre est un espace réservé et n'est pas pris en charge.*  <br/> |
|[EnumBlocks](ifreebusydata-enumblocks.md) <br/> |Obtient une interface qui énumère les blocs de données de disponibilité d'un utilisateur dans une plage de temps spécifiée.  <br/> |
|[Placeholder2](ifreebusydata-placeholder2.md) <br/> | *Ce membre est un espace réservé et n'est pas pris en charge.*  <br/> |
|[Placeholder3](ifreebusydata-placeholder3.md) <br/> | *Ce membre est un espace réservé et n'est pas pris en charge.*  <br/> |
|[Placeholder4](ifreebusydata-placeholder4.md) <br/> | *Ce membre est un espace réservé et n'est pas pris en charge.*  <br/> |
|[Placeholder5](ifreebusydata-placeholder5.md) <br/> | *Ce membre est un espace réservé et n'est pas pris en charge.*  <br/> |
|[SetFBRange](ifreebusydata-setfbrange.md) <br/> |Définit la plage de temps pour une énumération de blocs de données de disponibilité pour un utilisateur.  <br/> |
|[Placeholder6](ifreebusydata-placeholder6.md) <br/> | *Ce membre est un espace réservé et n'est pas pris en charge.*  <br/> |
|[GetFBPublishRange](ifreebusydata-getfbpublishrange.md) <br/> |Obtient une plage de temps prédéfinie pour une énumération de blocs de données de disponibilité pour un utilisateur.  <br/> |
   
## <a name="remarks"></a>Remarques

La plupart des membres de cette interface sont des espaces réservés réservés à l'usage interne d'Outlook et peuvent faire l'objet de modifications. Les fournisseurs de disponibilité doivent les implémenter uniquement comme spécifié, en renvoyant uniquement les valeurs de retour spécifiées.
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de type disponible/occupé](about-the-free-busy-api.md)
- [Constantes (API de disponibilité)](constants-free-busy-api.md)

