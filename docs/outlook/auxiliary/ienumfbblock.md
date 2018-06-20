---
title: IEnumFBBlock
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fad9c0fd-b523-db98-ee0d-78aad5914ff2
ms.openlocfilehash: 536c19aa314db9fca39298536c12464e71a71407
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782593"
---
# <a name="ienumfbblock"></a>IEnumFBBlock

Prend en charge l’accès et l’énumération des informations de disponibilité des blocs de données pour un utilisateur au sein d’une plage de temps.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Hérite de :  <br/> |[IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Fourni par :  <br/> |Fournisseur de disponibilité  <br/> |
|Identificateur de l’interface :  <br/> |**IEnumFBBlock** <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[Suivant](ienumfbblock-next.md) <br/> |Obtient le nombre spécifié suivant de blocs de données et de disponibilité dans une énumération.  <br/> |
|[Ignorer](ienumfbblock-skip.md) <br/> |Ignore un nombre spécifié de blocs de données et de disponibilité.  <br/> |
|[Reset](ienumfbblock-reset.md) <br/> |Réinitialise l’énumérateur en définissant le curseur au début.  <br/> |
|[Clone](ienumfbblock-clone.md) <br/> |Crée une copie de l’énumérateur, à l’aide de la même restriction mais définissant le curseur au début de l’énumérateur.  <br/> |
|[Restreindre](ienumfbblock-restrict.md) <br/> |Limite de l’énumération à une période spécifiée.  <br/> |
   
## <a name="remarks"></a>Remarques

Une énumération contient des informations de disponibilité des blocs de données qui ne se chevauchent pas dans le temps. Lorsqu’il existe des éléments qui se chevauchent dans un calendrier, Outlook fusionne ces éléments pour former des blocs de disponibilité sans chevauchement de l’énumération basée sur cet ordre de priorité : hors du bureau, provisoire, occupé (e).
  
Un fournisseur et de disponibilité permet d’obtenir cette interface et l’énumération pour une plage de temps pour un utilisateur par le biais de [IFreeBusyData](ifreebusydata.md).
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de type disponible/occupé](about-the-free-busy-api.md)  
- [Constantes (disponibilité API)](constants-free-busy-api.md)  
- [IFreeBusyData](ifreebusydata.md)

