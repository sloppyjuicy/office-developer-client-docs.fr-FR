---
title: MAPIAdminProfiles
description: Décrit la fonction MAPIAdminProfiles et fournit la syntaxe, les paramètres, la valeur de retour et les références MFCMAPI.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPIAdminProfiles
api_type:
- HeaderDef
ms.assetid: 82a9e379-39e4-4257-8cba-a6758f431cdc
ms.openlocfilehash: e61c16fa4bd0142c317cbfd27cd96592a1e65dac
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817696"
---
# <a name="mapiadminprofiles"></a>MAPIAdminProfiles

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un objet d’administration de profil. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapix.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
   
```cpp
HRESULT MAPIAdminProfiles(
  ULONG ulFlags,
  LPPROFADMIN FAR * lppProfAdmin
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits des indicateurs indiquant les options de la fonction d’entrée de service. 
    
 _lppProfAdmin_
  
> [out] Pointeur vers un pointeur vers le nouvel objet d’administration de profil.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::GetProfAdmin  <br/> |MFCMAPI utilise la méthode **MAPIAdminProfiles** pour obtenir l’objet d’administration de profil. |
   
## <a name="see-also"></a>Voir aussi



[IProfAdmin::CreateProfile](iprofadmin-createprofile.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

