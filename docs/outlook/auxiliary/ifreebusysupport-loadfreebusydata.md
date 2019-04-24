---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Renvoie, pour chaque utilisateur spécifié, une interface permettant d'énumérer les blocs de données de disponibilité au sein d'un intervalle de temps.
ms.openlocfilehash: e55f902117a20bfefaa5d9a2f3a067cb78ec86cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319403"
---
# <a name="ifreebusysupportloadfreebusydata"></a>IFreeBusySupport::LoadFreeBusyData

Renvoie, pour chaque utilisateur spécifié, une interface permettant d'énumérer les blocs de données de disponibilité au sein d'un intervalle de temps. 
  
## <a name="quick-info"></a>Informations rapides

Voir [IFreeBusySupport](ifreebusysupport.md).
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a>Paramètres

_cMax_
  
> dans Nombre d'interfaces [IFreeBusyData](ifreebusydata.md) à renvoyer. 
    
_rgfbuser_
  
> dans Tableau des utilisateurs de disponibilité pour lesquels récupérer des données.
    
_prgfbdata_
  
> dans remarquer Tableau des interfaces **IFreeBusyData** qui correspondent au tableau _Rgfbuser_ des structures [FBUser](fbuser.md) . 
    
   > [!NOTE]
   > Ce tableau de pointeurs est alloué par l'appelant et libéré par l'appelant. Les interfaces réelles pointant vers sont libérées lorsque l'appelant les a réalisées. 
  
_phrStatus_
  
> remarquer Tableau de résultats **HRESULT** permettant de récupérer chaque interface **IFreeBusyData** correspondante. La valeur peut être NULL. Un résultat est défini sur S_OK si _prgfbdata_ correspondant est valide. 
    
_pcRead_
  
>  remarquer Nombre réel d'utilisateurs pour lesquels une interface **IFreeBusyData** a été trouvée. 
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de disponibilité)](constants-free-busy-api.md)

