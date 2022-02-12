---
title: IProfAdminGetProfileTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfAdmin.GetProfileTable
api_type:
- COM
ms.assetid: cebccd2d-8215-486e-9964-7fc42412cec6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5e512fc485bf7cff18a422c61be835b40146df45
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62789129"
---
# <a name="iprofadmingetprofiletable"></a>IProfAdmin::GetProfileTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet d’accéder à la table de profils, qui contient des informations sur tous les profils disponibles.
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Toujours NULL.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers le tableau de profil.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table de profil a été récupérée avec succès.
    
## <a name="remarks"></a>Remarques

La **méthode IProfAdmin::GetProfileTable** permet d’accéder à la table de profils, qui contient une ligne pour chaque profil disponible. Chaque ligne ne compte que deux colonnes : le nom complet du profil et un indicateur qui indique si le profil est la valeur par défaut. 
  
Les profils qui ont été supprimés ou qui sont en cours d’utilisation mais qui ont été marqués pour suppression ne sont pas inclus dans la table de profils. La table de profils est statique ; Les ajouts et suppressions de profils ultérieurs ne sont pas reflétés dans le tableau. 
  
S’il n’existe aucun **profil, GetProfileTable renvoie** un tableau avec zéro ligne. 
  
Pour plus d’informations sur la table de profils, voir [Tables de profils](profile-tables.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnShowProfiles  <br/> |MFCMAPI utilise la méthode **IProfAdmin::GetProfileTable** pour obtenir la table de profil à afficher dans une nouvelle boîte de dialogue. |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable : IUnknown](imapitableiunknown.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

