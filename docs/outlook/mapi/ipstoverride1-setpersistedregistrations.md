---
title: IPSTOVERRIDE1SetPersistedRegistrations
description: IPSTOVERRIDE1 SetPersistedRegistrations inscrit les fichiers Dossiers personnels (.pst) pour le déverrouillage automatique.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPSTOVERRIDE1.SetPersistedRegistrations
api_type:
- COM
ms.assetid: 5f4b62db-a759-41a2-9bea-29fc04b2962b
ms.openlocfilehash: 270fb821d81c363050edc800e16b8b2017a1bb92
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828275"
---
# <a name="ipstoverride1setpersistedregistrations"></a>IPSTOVERRIDE1::SetPersistedRegistrations

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Inscrit les fichiers Dossiers personnels (.pst) pour le déverrouillage automatique, en évitant d’autres appels à HrTrustedPSTOverrideHandlerCallback.
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a>Paramètres

_pmval_
  
> [in] Structure [SPropValue](spropvalue.md) qui contient un pointeur vers le chemin d’accès de la bibliothèque de liens dynamiques (DLL) à inscrire. La structure présente les caractéristiques suivantes : 
    
   - UlPropTag de [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).
    
   - Propriété de valeur MVszW définie sur un tableau de chaînes de caractères Unicode terminées par une valeur Null. Pour plus d’informations, consultez la rubrique [SWStringArray](swstringarray.md) . 
    
> [!NOTE]
> Le SPropValue est stocké dans une propriété MAPI dans la plage interne du PST. Cette propriété est inaccessible aux applications MAPI ordinaires. 
  
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel de fonction a réussi.
    
## <a name="remarks"></a>Remarques

Les inscriptions persistantes peuvent nuire aux performances des applications, telles que Outlook et Windows Desktop Search, qui ouvrent des rtc. Tenez compte de l’effet sur les performances lors de l’utilisation ou de l’extension de l’utilisation des inscriptions persistantes.
  
> [!IMPORTANT]
> Cette méthode est implémentée pour Unicode uniquement. En outre, elle échoue de manière préventive si l’un des chemins d’accès du tableau n’a pas d’extension de nom de fichier de .dll. 
  
## <a name="see-also"></a>Voir aussi

- [IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md) 
- [IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

