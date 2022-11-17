---
title: IMsgStoreGetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.GetReceiveFolder
api_type:
- COM
ms.assetid: ccd9d623-a3cb-4e66-9649-78c3887cb726
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fbe14827f7d762fe85af7bc7a535f41f78d9496e
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62463218"
---
# <a name="imsgstoregetreceivefolder"></a>IMsgStore::GetReceiveFolder

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Obtient le dossier qui a été établi comme destination pour les messages entrants d’une classe de message spécifiée ou comme dossier de réception par défaut pour la magasin de messages.
  
```cpp
HRESULT GetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID,
  LPSTR FAR * lppszExplicitClass
);
```

## <a name="parameters"></a>Paramètres

 _lpszMessageClass_
  
> [in] Pointeur vers une classe de message associée à un dossier de réception. Si le  _paramètre lpszMessageClass_ a la valeur NULL ou une chaîne vide, **GetReceiveFolder** renvoie le dossier de réception par défaut pour la magasin de messages. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type des chaînes transmises et renvoyées. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> La chaîne de classe de message est au format Unicode. Si l’MAPI_UNICODE n’est pas définie, la chaîne de classe de message est au format ANSI.
    
 _lpcbEntryID_
  
> [out] Pointeur vers le nombre d’byte dans l’identificateur d’entrée pointé par  _le paramètre lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée pour le dossier de réception demandé.
    
 _lppszExplicitClass_
  
> [out] Pointeur vers un pointeur vers la classe de message qui définit explicitement comme dossier de réception le dossier pointé par  _lppEntryID_. Cette classe de message doit être la même que la classe dans le paramètre _lpszMessageClass_ ou une classe de base de cette classe. La transmission de la valeur NULL indique que le dossier pointé par  _lppEntryID_ est le dossier de réception par défaut pour la magasin de messages. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le dossier de réception a été renvoyé avec succès.
    
## <a name="remarks"></a>Remarques

La **méthode IMsgStore::GetReceiveFolder** obtient l’identificateur d’entrée d’un dossier de réception, un dossier désigné pour recevoir les messages entrants d’une classe de message particulière. Les appelants peuvent spécifier une classe de message ou null dans _le paramètre lpszMessageClass_ . Si  _lpszMessageClass a_ la valeur NULL, **GetReceiveFolder** renvoie les valeurs suivantes : 
  
- Dans  _lppszExplicitClass_, le nom de la première classe de base de la classe de message pointée par  _lpszMessageClass_ qui définisse explicitement un dossier de réception. 
    
- Dans  _lppEntryID_, l’identificateur d’entrée du dossier de réception pour la classe de base pointée par le paramètre  _lppszExplicitClass_ . 
    
Par exemple, supposons que le dossier de réception de la classe **de message IPM. Note** has been set to the entry identifier of the Inbox and **GetReceiveFolder** is called with the contents of _lpszMessageClass_ set to **IPM. Remarque. Téléphone**. Si **IPM. Remarque. Téléphone** n’a pas de dossier de réception explicite, **GetReceiveFolder** renvoie l’identificateur d’entrée de la boîte de réception dans _lppEntryID_ et **IPM. Remarque** dans _lppszExplicitClass_.
  
Si le client appelle **GetReceiveFolder** pour une classe de message et n’a pas de dossier de réception pour cette classe de message,  _lppszExplicitClass_ est une chaîne de longueur nulle, une chaîne au format Unicode ou une chaîne au format ANSI selon que le client a ou non définie l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ . 
  
Un dossier de réception par défaut, obtenu en passant la valeur NULL dans le paramètre _lpszMessageClass_ , existe toujours pour chaque magasin de messages. 
  
Un client doit appeler la [fonction MAPIFreeBuffer](mapifreebuffer.md) lorsqu’elle est effectuée avec l’identificateur d’entrée renvoyé dans  _lppEntryID_ pour libérer la mémoire qui contient cet identificateur d’entrée. Il doit également appeler **MAPIFreeBuffer** lorsqu’il est terminé avec la chaîne de classe de message renvoyée dans  _lppszExplicitClass_ pour libérer la mémoire qui contient cette chaîne. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetInbox  <br/> |MFCMAPI utilise la **méthode IMsgStore::GetReceiveFolder** pour localiser le dossier Boîte de réception.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

