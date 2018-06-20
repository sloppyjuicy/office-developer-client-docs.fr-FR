---
title: IFreeBusyData
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c9a80ad3-6311-fe07-b6f7-9fd63424753b
ms.openlocfilehash: aa42561277d5fc4de93eeedec8ceb6f36530fb80
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782589"
---
# <a name="ifreebusydata"></a>IFreeBusyData

Pour un utilisateur donné, obtient et définit une plage de temps et renvoie une interface pour énumérer les informations de disponibilité des blocs de données dans cette plage de temps.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Hérite de :  <br/> |[IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Fourni par :  <br/> |Fournisseur de disponibilité  <br/> |
|Identificateur de l’interface :  <br/> |IID_IFreeBusyData  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[PlaceHolder1](ifreebusydata-placeholder1.md) <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
|[EnumBlocks](ifreebusydata-enumblocks.md) <br/> |Obtient une interface qui énumère les informations de disponibilité des blocs de données pour un utilisateur au sein d’une plage de temps spécifié.  <br/> |
|[Espace_réservé2](ifreebusydata-placeholder2.md) <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
|[Placeholder3](ifreebusydata-placeholder3.md) <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
|[Placeholder4](ifreebusydata-placeholder4.md) <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
|[Placeholder5](ifreebusydata-placeholder5.md) <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
|[SetFBRange](ifreebusydata-setfbrange.md) <br/> |Définit l’intervalle de temps pour une énumération des blocs de données de disponibilité d’un utilisateur.  <br/> |
|[Placeholder6](ifreebusydata-placeholder6.md) <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
|[GetFBPublishRange](ifreebusydata-getfbpublishrange.md) <br/> |Obtient une énumération des informations de disponibilité des blocs de données pour un utilisateur une plage de temps prédéfini.  <br/> |
   
## <a name="remarks"></a>Remarques

La plupart des membres de cette interface est des espaces réservés réservé à un usage interne d’Outlook et est sujettes à modification. Fournisseurs de disponibilité doivent les implémenter comme spécifié, renvoi de que valeurs de retour uniquement spécifié.
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de type disponible/occupé](about-the-free-busy-api.md)
- [Constantes (disponibilité API)](constants-free-busy-api.md)

