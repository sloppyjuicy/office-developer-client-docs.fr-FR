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
ms.openlocfilehash: 2db7dba67e7b71df6921ecd97189255a0ef7823a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309547"
---
# <a name="iprofadmingetprofiletable"></a>IProfAdmin::GetProfileTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit l'accès à la table de profils, une table qui contient des informations sur tous les profils disponibles.
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Toujours NULL.
    
 _lppTable_
  
> remarquer Pointeur vers un pointeur vers le tableau de profils.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table de profils a été correctement récupérée.
    
## <a name="remarks"></a>Remarques

La méthode **IProfAdmin:: GetProfileTable** fournit l'accès à la table de profils, qui contient une ligne pour chaque profil disponible. Chaque ligne comporte uniquement deux colonnes: le nom d'affichage du profil et un indicateur qui indique si le profil est la valeur par défaut. 
  
Les profils qui ont été supprimés, ou qui sont en cours d'utilisation mais qui ont été marqués pour suppression, ne sont pas inclus dans la table de profils. La table de profils est statique; les ajouts et suppressions de profils suivants ne sont pas répercutés dans le tableau. 
  
Si aucun profil n'existe, **GetProfileTable** renvoie un tableau sans aucune ligne. 
  
Pour plus d'informations sur la table de profils, voir [Profile tables](profile-tables.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg. cpp  <br/> |CMainDlg:: OnShowProfiles  <br/> |MFCMAPI utilise la méthode **IProfAdmin:: GetProfileTable** pour obtenir la table de profil à afficher dans une nouvelle boîte de dialogue.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable : IUnknown](imapitableiunknown.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

