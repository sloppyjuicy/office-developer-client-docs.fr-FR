---
title: IEnumFBBlock
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: fad9c0fd-b523-db98-ee0d-78aad5914ff2
ms.openlocfilehash: c357f8ed9eb8fe9fd401aacfa58728a17b0fe199
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63783027"
---
# <a name="ienumfbblock"></a>IEnumFBBlock

Prend en charge l’accès et l’éumation des blocs de données de libre/occupé pour un utilisateur dans un délai.
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Hérite de :  <br/> |[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Fourni par :  <br/> |Fournisseur de services de libre-service  <br/> |
|Identificateur d’interface :  <br/> |**IEnumFBBlock** <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|Member |Description |
|:-----|:-----|
|[Next](ienumfbblock-next.md) <br/> |Obtient le nombre spécifié suivant de blocs de données de libre/occupé dans une éumération. |
|[Skip](ienumfbblock-skip.md) <br/> |Ignore un nombre spécifié de blocs de données de libre/occupé. |
|[Reset](ienumfbblock-reset.md) <br/> |Réinitialise l’éumérateur en  redéfinissant le curseur au début. |
|[Clone](ienumfbblock-clone.md) <br/> |Crée une copie de l’éumérateur, en utilisant la même restriction de temps, mais en lui fixant le début de l’éumérateur. |
|[Restrict](ienumfbblock-restrict.md) <br/> |Limite l’éumération à une période spécifiée. |
   
## <a name="remarks"></a>Remarques

Une éumération contient des blocs de données de libre/occupé qui ne se chevauchent pas dans le temps. Lorsqu’un calendrier se chevauche, Outlook fusionne ces éléments pour former des blocs de libre/occupé non superposés dans l’éumération en fonction de cet ordre de priorité : absence du bureau, occupé, provisoire.
  
Un fournisseur de libre/occupé obtient cette interface et l’éumération pour un délai d’un utilisateur via [IFreeBusyData](ifreebusydata.md).
  
## <a name="see-also"></a>Voir aussi

- [À propos de l’API Disponibilité](about-the-free-busy-api.md)  
- [Constantes (API de libre/occupé)](constants-free-busy-api.md)  
- [IFreeBusyData](ifreebusydata.md)

