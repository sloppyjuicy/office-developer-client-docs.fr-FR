---
title: IProfAdminGetProfileTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetProfileTable
api_type:
- COM
ms.assetid: cebccd2d-8215-486e-9964-7fc42412cec6
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c942bdbf27590dde04b84970e345f265bc645045
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784385"
---
# <a name="iprofadmingetprofiletable"></a>IProfAdmin::GetProfileTable

  
  
**S’applique à**: Outlook 
  
Permet d’accéder à la table de profil, un tableau qui contient des informations sur tous les profils disponibles.
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Toujours NULL.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers la table de profils.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le tableau de profil a été récupéré correctement.
    
## <a name="remarks"></a>Remarques

La méthode **IProfAdmin::GetProfileTable** permet d’accéder à la table de profil, qui contient une ligne pour chaque profil disponible. Il existe deux colonnes dans chaque ligne : nom d’affichage du profil et d’un indicateur qui indique si le profil est la valeur par défaut. 
  
Profils qui ont été supprimés, ou qui ont été marquées pour suppression, mais qui sont en cours d’utilisation ne sont pas inclus dans la table de profils. Le tableau de profil est statique ; les ajouts et suppressions de profils ne sont pas reflétées dans la table. 
  
Si aucun profil n’existe pas, **GetProfileTable** renvoie un tableau avec des lignes de zéro. 
  
Pour plus d’informations sur la table de profils, voir [Les Tables de profil](profile-tables.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnShowProfiles  <br/> |MFCMAPI utilise la méthode **IProfAdmin::GetProfileTable** pour obtenir le tableau de profil à afficher dans une boîte de dialogue.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable : IUnknown](imapitableiunknown.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

