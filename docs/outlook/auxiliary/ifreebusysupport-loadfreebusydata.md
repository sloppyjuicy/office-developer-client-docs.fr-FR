---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Renvoie, pour chaque utilisateur spécifié, une interface pour énumérer les informations de disponibilité des blocs de données au sein d’une plage de temps.
ms.openlocfilehash: 9af5a40da9f0a831de7346b44cee9ca004c02300
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782586"
---
# <a name="ifreebusysupportloadfreebusydata"></a>IFreeBusySupport::LoadFreeBusyData

Renvoie, pour chaque utilisateur spécifié, une interface pour énumérer les informations de disponibilité des blocs de données au sein d’une plage de temps. 
  
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
  
> [in] Le nombre d’interfaces [IFreeBusyData](ifreebusydata.md) à renvoyer. 
    
_rgfbuser_
  
> [in] Le tableau de disponibilité pour les utilisateurs à récupérer des données pour.
    
_prgfbdata_
  
> [in] [out] Tableau des interfaces **IFreeBusyData** qui correspondent au tableau de structures [FBUser](fbuser.md) _rgfbuser_ . 
    
   > [!NOTE]
   > Ce tableau de pointeurs est alloué par l’appelant et libéré par l’appelant. Les interfaces réels vers lequel pointés sont libérées lorsque l’appelant est terminé avec eux. 
  
_phrStatus_
  
> [out] Le tableau de résultats **HRESULT** pour l’extraction de chaque interface **IFreeBusyData** correspondante. La valeur peut être NULL. Un résultat est défini à S_OK si correspondante _prgfbdata_ n’est valide. 
    
_pcRead_
  
>  [out] Le nombre d’utilisateurs pour lequel une interface **IFreeBusyData** a été détectée. 
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="see-also"></a>Voir aussi

- [Constantes (disponibilité API)](constants-free-busy-api.md)

