---
title: IMsgStoreSetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.SetReceiveFolder
api_type:
- COM
ms.assetid: 469f0412-1343-47ce-b6e8-e0d5e56c29bb
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d1211ee2e096e59b92d4e05c22a7abc29ccdc8f9
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62777396"
---
# <a name="imsgstoresetreceivefolder"></a>IMsgStore::SetReceiveFolder

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Établit un dossier comme destination pour les messages entrants d’une classe de message particulière.
  
```cpp
HRESULT SetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Paramètres

 _lpszMessageClass_
  
> [in] Pointeur vers la classe de message à associer au nouveau dossier de réception. Si le  _paramètre lpszMessageClass_ a la valeur NULL ou une chaîne vide, **SetReceiveFolder** définit le dossier de réception par défaut pour la magasin de messages. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type du texte dans les chaînes transmises. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> La chaîne de classe de message est au format Unicode. Si l’MAPI_UNICODE n’est pas définie, la chaîne de classe de message est au format ANSI.
    
 _cbEntryID_
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par  _le paramètre lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du dossier à établir en tant que dossier de réception. Si le  _paramètre lpEntryID_ est définie sur NULL, **SetReceiveFolder** remplace le dossier de réception actuel par la valeur par défaut de la boutique de messages. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Un dossier de réception a été correctement établi.
    
## <a name="remarks"></a>Remarques

La **méthode IMsgStore::SetReceiveFolder** définit ou modifie le dossier de réception d’une classe de message particulière. Avec **SetReceiveFolder**, un client peut, à l’aide d’appels successifs, spécifier un dossier de réception différent pour chaque classe de message définie ou spécifier que les messages entrants pour plusieurs classes de messages sont tous placés dans le même dossier. Par exemple, un client peut avoir sa propre classe de messages arrive dans son propre dossier. Une application de télécopie peut désigner un dossier dans lequel le fournisseur de magasins place les télécopies entrantes et un autre dossier dans lequel le fournisseur place les télécopies sortantes.
  
Si une erreur se produit pendant l’appel de **SetReceiveFolder**, le paramètre du dossier de réception reste inchangé. 
  
Si **SetReceiveFolder** modifie le paramètre du dossier de réception avec  _lpEntryID_ définie sur NULL, indiquant que le dossier de réception par défaut doit être définie, **SetReceiveFolder** renvoie S_OK même s’il n’y avait aucun paramètre existant pour la classe de message indiquée. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnSetReceiveFolder  <br/> |MFCMAPI utilise la méthode **IMsgStore::SetReceiveFolder** pour définir un dossier comme dossier de réception pour une classe de message particulière. |
   
## <a name="see-also"></a>Voir aussi



[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

