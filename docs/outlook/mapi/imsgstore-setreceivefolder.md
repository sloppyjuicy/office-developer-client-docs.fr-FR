---
title: IMsgStoreSetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.SetReceiveFolder
api_type:
- COM
ms.assetid: 469f0412-1343-47ce-b6e8-e0d5e56c29bb
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: efa5d60098fd5f16328669249a8445a124d9878b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434087"
---
# <a name="imsgstoresetreceivefolder"></a>IMsgStore::SetReceiveFolder

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Établit un dossier comme destination pour les messages entrants d'une classe de message particulière.
  
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
  
> dans Pointeur vers la classe de message qui doit être associée au nouveau dossier de réception. Si le paramètre _lpszMessageClass_ est défini sur null ou sur une chaîne vide, **SetReceiveFolder** définit le dossier de réception par défaut pour la Banque de messages. 
    
 _ulFlags_
  
> dans Masque de bits des indicateurs qui contrôle le type du texte dans les chaînes transmises. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> La chaîne de la classe de message est au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, la chaîne de la classe de message est au format ANSI.
    
 _cbEntryID_
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> dans Pointeur vers l'identificateur d'entrée du dossier à établir en tant que dossier de réception. Si le paramètre _lpEntryID_ est défini sur null, **SetReceiveFolder** remplace le dossier de réception actuel par la valeur par défaut de la Banque de messages. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Un dossier de réception a été correctement établi.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgStore:: SetReceiveFolder** définit ou modifie le dossier de réception d'une classe de message particulière. Avec **SetReceiveFolder**, un client peut, en utilisant des appels successifs, spécifier un autre dossier de réception pour chaque classe de message définie ou spécifier que les messages entrants pour plusieurs classes de message accèdent au même dossier. Par exemple, un client peut avoir sa propre classe de messages arrivant dans son propre dossier. Une application de télécopie peut désigner un dossier dans lequel le fournisseur de banque d'applications place les télécopies entrantes et un autre dossier dans lequel le fournisseur place les télécopies sortantes.
  
Si une erreur se produit lors de l'appel à **SetReceiveFolder**, le paramètre de dossier de réception reste inchangé. 
  
Si **SetReceiveFolder** remplace le paramètre de dossier de réception par _lpEntryID_ par null, ce qui indique que le dossier de réception par défaut doit être défini, **SetReceiveFolder** renvoie S_OK même s'il n'existe aucun paramètre pour le spécifié classe de message. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgStoreDlg. cpp  <br/> |CMsgStoreDlg:: OnSetReceiveFolder  <br/> |MFCMAPI utilise la méthode **IMsgStore:: SetReceiveFolder** pour définir un dossier en tant que dossier de réception pour une classe de message particulière.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

