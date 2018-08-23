---
title: IPSTOVERRIDE1SetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1.SetPersistedRegistrations
api_type:
- COM
ms.assetid: 5f4b62db-a759-41a2-9bea-29fc04b2962b
description: 'Dernière modification : 08 novembre 2011'
ms.openlocfilehash: 3592584a08bf14725c0289831740e91fb8f1a5b2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587620"
---
# <a name="ipstoverride1setpersistedregistrations"></a>IPSTOVERRIDE1::SetPersistedRegistrations

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Enregistre les fichiers de dossiers personnels (.pst) pour le déverrouillage automatique, en évitant les appels supplémentaires à la HrTrustedPSTOverrideHandlerCallback.
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a>Paramètres

_pmval_
  
> [in] Contient un pointeur vers le chemin d’accès de la bibliothèque de liens dynamiques (DLL) pour inscrire une structure [SPropValue](spropvalue.md) . La structure présente les caractéristiques suivantes : 
    
   - Un ulPropTag de [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).
    
   - Une propriété de valeur MVszW qui est définie sur un tableau de chaînes de caractères Unicode terminée par null. Pour plus d’informations, consultez la rubrique [SWStringArray](swstringarray.md) . 
    
> [!NOTE]
> Le SPropValue est stocké dans une propriété MAPI dans une plage interne du fichier PST. Cette propriété n’est pas accessible pour les applications MAPI ordinaires. 
  
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’appel de fonction a réussi.
    
## <a name="remarks"></a>Remarques

Les enregistrements persistants peuvent affecter les performances des applications, tels qu’Outlook et Windows Desktop Search, ouvrez les fichiers pst. Prendre en compte l’impact sur les performances lors de l’aide ou développer l’utilisation des enregistrements persistants.
  
> [!IMPORTANT]
> Cette méthode est implémentée uniquement pour le format Unicode. En outre, il façon préventive échoue si un des chemins d’accès dans le tableau n’ont pas une extension de nom de fichier du fichier .dll. 
  
## <a name="see-also"></a>Voir aussi

- [IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md) 
- [IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

