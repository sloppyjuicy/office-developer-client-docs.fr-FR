---
title: IFreeBusyData
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c9a80ad3-6311-fe07-b6f7-9fd63424753b
ms.openlocfilehash: 53e9bcca19eb9f7e8bea391319c43ec0a01fd625
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63631238"
---
# <a name="ifreebusydata"></a>IFreeBusyData

Pour un utilisateur donné, obtient et définit un délai et renvoie une interface pour l’éumation des blocs de données de la période.
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Hérite de :  <br/> |[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Fourni par :  <br/> |Fournisseur de services de libre-service  <br/> |
|Identificateur d’interface :  <br/> |IID_IFreeBusyData  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|Member |Description |
|:-----|:-----|
|[Placeholder1](ifreebusydata-placeholder1.md) <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
|[EnumBlocks](ifreebusydata-enumblocks.md) <br/> |Obtient une interface qui éumène les blocs de données de libre/occupé pour un utilisateur dans un délai spécifié. |
|[Placeholder2](ifreebusydata-placeholder2.md) <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
|[Placeholder3](ifreebusydata-placeholder3.md) <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
|[Placeholder4](ifreebusydata-placeholder4.md) <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
|[Placeholder5](ifreebusydata-placeholder5.md) <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
|[SetFBRange](ifreebusydata-setfbrange.md) <br/> |Définit la plage de temps pour une éumération des blocs de données de la période de libre/occupé d’un utilisateur. |
|[Placeholder6](ifreebusydata-placeholder6.md) <br/> | *Ce membre est un espace réservé et n’est pas pris en charge.*  <br/> |
|[GetFBPublishRange](ifreebusydata-getfbpublishrange.md) <br/> |Obtient une plage de temps prédéfinie pour une éumération des blocs de données de libre/occupé d’un utilisateur. |
   
## <a name="remarks"></a>Remarques

La plupart des membres de cette interface sont des espaces réservés à l’utilisation interne des Outlook et peuvent faire l’objet de changements. Les fournisseurs de libre/occupé doivent les implémenter uniquement comme spécifié, en renvoyant uniquement les valeurs de retour spécifiées.
  
## <a name="see-also"></a>Consultez aussi

- [À propos de l’API Disponibilité](about-the-free-busy-api.md)
- [Constantes (API de libre/occupé)](constants-free-busy-api.md)

