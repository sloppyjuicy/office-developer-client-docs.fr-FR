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

Prend en charge l’accès et l’éumation des blocs de données de libre/occupé pour un utilisateur dans un délai.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Hérite de :  <br/> |[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Fourni par :  <br/> |Fournisseur de services de libre-service  <br/> |
|Identificateur d’interface :  <br/> |**IEnumFBBlock** <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[Next](ienumfbblock-next.md) <br/> |Obtient le nombre spécifié suivant de blocs de données de libre/occupé dans une éumération.  <br/> |
|[Skip](ienumfbblock-skip.md) <br/> |Ignore un nombre spécifié de blocs de données de libre/occupé.  <br/> |
|[Reset](ienumfbblock-reset.md) <br/> |Réinitialise l’éumérateur en redéfinissant le curseur au début.  <br/> |
|[Clone](ienumfbblock-clone.md) <br/> |Crée une copie de l’éumérateur, en utilisant la même restriction de temps, mais en lui fixant le début de l’éumérateur.  <br/> |
|[Restrict](ienumfbblock-restrict.md) <br/> |Limite l’éumération à une période spécifiée.  <br/> |
   
## <a name="remarks"></a>Remarques

Une éumération contient des blocs de données de libre/occupé qui ne se chevauchent pas dans le temps. Lorsqu’un calendrier se chevauche, Outlook fusionne ces éléments pour former des blocs de libre/occupé non superposés dans l’éumération en fonction de cet ordre de priorité : absence du bureau, occupé, provisoire.
  
Un fournisseur de libre/occupé obtient cette interface et l’éumération pour un délai d’un utilisateur via [IFreeBusyData](ifreebusydata.md).
  
## <a name="see-also"></a>Voir aussi

- [À propos de l’API Disponibilité](about-the-free-busy-api.md)  
- [Constantes (API de libre/occupé)](constants-free-busy-api.md)  
- [IFreeBusyData](ifreebusydata.md)

