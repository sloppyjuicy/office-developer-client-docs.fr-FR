---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Renvoie, pour chaque utilisateur spécifié, une interface pour l’éumation des blocs de données de libre/occupé dans un délai.
ms.openlocfilehash: e55f902117a20bfefaa5d9a2f3a067cb78ec86cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411231"
---
# <a name="ifreebusysupportloadfreebusydata"></a>IFreeBusySupport::LoadFreeBusyData

Renvoie, pour chaque utilisateur spécifié, une interface pour l’éumation des blocs de données de libre/occupé dans un délai. 
  
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
  
> [in] Nombre d’interfaces [IFreeBusyData](ifreebusydata.md) à renvoyer. 
    
_rgfbuser_
  
> [in] Tableau des utilisateurs de la période de libre/occupé pour qui récupérer des données.
    
_prgfbdata_
  
> [in] [out] Tableau des interfaces **IFreeBusyData** qui correspondent au tableau _rgfbuser_ des structures [FBUser.](fbuser.md) 
    
   > [!NOTE]
   > Ce tableau de pointeurs est alloué par l’appelant et libéré par l’appelant. Les interfaces réelles pointées vers sont libérées lorsque l’appelant a terminé de les utiliser. 
  
_phrStatus_
  
> [out] Tableau des résultats **HRESULT** pour la récupération de chaque interface **IFreeBusyData** correspondante. La valeur peut être NULL. Un résultat est S_OK si  _prgfbdata_ est valide. 
    
_pcRead_
  
>  [out] Nombre réel d’utilisateurs pour lesquels une interface **IFreeBusyData** a été trouvée. 
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de libre/occupé)](constants-free-busy-api.md)

