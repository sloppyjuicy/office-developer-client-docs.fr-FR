---
title: IPSTOVERRIDE1SetPersistedRegistrations
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
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: 0d5ebfe46d34c8ba2381900d445f47bd5ea08215
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587859"
---
# <a name="ipstoverride1setpersistedregistrations"></a>IPSTOVERRIDE1::SetPersistedRegistrations

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Enregistre les fichiers de dossiers personnels (.pst) pour le déverrouillage automatique, en évitant d’autres appels à HrTrustedPSTOverrideHandlerCallback.
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a>Paramètres

_pmval_
  
> [in] Structure [SPropValue](spropvalue.md) qui contient un pointeur vers le chemin d’accès de la bibliothèque de liens dynamiques (DLL) à inscrire. La structure présente les caractéristiques suivantes : 
    
   - UlPropTag de [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).
    
   - Propriété de valeur MVszW définie sur un tableau de chaînes de caractères Unicode terminées par null. Pour plus d’informations, [voir la rubrique SWStringArray.](swstringarray.md) 
    
> [!NOTE]
> La valeur SPropValue est stockée dans une propriété MAPI dans la plage interne du PST. Cette propriété n’est pas accessible aux applications MAPI ordinaires. 
  
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel de fonction a réussi.
    
## <a name="remarks"></a>Remarques

Les inscriptions persistantes peuvent nuire aux performances des applications, telles que Outlook et Windows Desktop Search, qui ouvrent des PST. Prenons en compte l’impact sur les performances lors de l’utilisation ou de l’extension de l’utilisation d’inscriptions persistantes.
  
> [!IMPORTANT]
> Cette méthode est implémentée pour Unicode uniquement. En outre, elle échouera de manière préemptive si l’un des chemins d’accès du tableau n’a pas d’extension de nom de fichier .dll. 
  
## <a name="see-also"></a>Voir aussi

- [IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md) 
- [IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

