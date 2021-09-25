---
title: IEnumFBBlock
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: fad9c0fd-b523-db98-ee0d-78aad5914ff2
ms.openlocfilehash: 99c61a576061daec4ab6916bda1a62efe93dffd5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564595"
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
|[Clone](ienumfbblock-clone.md) <br/> |Crée une copie de l’éumérateur, en utilisant la même restriction de temps, mais en fixant le curseur au début de l’éumérateur.  <br/> |
|[Restrict](ienumfbblock-restrict.md) <br/> |Limite l’éumération à une période spécifiée.  <br/> |
   
## <a name="remarks"></a>Remarques

Une éumération contient des blocs de données de libre/occupé qui ne se chevauchent pas dans le temps. Lorsqu’un calendrier se chevauche, Outlook fusionne ces éléments pour former des blocs de libre/occupé non superposés dans l’éumération en fonction de cet ordre de priorité : absence du bureau, occupé, provisoire.
  
Un fournisseur de libre/occupé obtient cette interface et l’éumération pour un délai d’un utilisateur via [IFreeBusyData](ifreebusydata.md).
  
## <a name="see-also"></a>Voir aussi

- [À propos de l’API Disponibilité](about-the-free-busy-api.md)  
- [Constantes (API de libre/occupé)](constants-free-busy-api.md)  
- [IFreeBusyData](ifreebusydata.md)

