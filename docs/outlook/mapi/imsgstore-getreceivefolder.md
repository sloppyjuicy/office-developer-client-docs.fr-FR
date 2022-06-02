---
title: IMsgStoreGetReceiveFolder
description: IMsgStore GetReceiveFolder obtient le dossier qui a été établi comme destination pour les messages entrants d’une classe de message spécifiée.
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
ms.openlocfilehash: 8bc282b7e96fd7f8a45fc5a38348720d4b67af6e
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828310"
---
# <a name="imsgstoregetreceivefolder"></a>IMsgStore::GetReceiveFolder

**S’applique à** : Outlook 2013 | Outlook 2016
  
Obtient le dossier qui a été établi comme destination pour les messages entrants d’une classe de message spécifiée ou comme dossier de réception par défaut pour le magasin de messages.
  
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
  
> [in] Pointeur vers une classe de message associée à un dossier de réception. Si le paramètre _lpszMessageClass_ a la valeur NULL ou une chaîne vide, **GetReceiveFolder** renvoie le dossier de réception par défaut pour le magasin de messages.

 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle le type des chaînes passées et retournées. L’indicateur suivant peut être défini :

MAPI_UNICODE
  
> La chaîne de classe de message est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, la chaîne de classe de message est au format ANSI.

 _lpcbEntryID_
  
> [out] Pointeur vers le nombre d’octets dans l’identificateur d’entrée pointé par le paramètre _lppEntryID_ .

 _lppEntryID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée pour le dossier de réception demandé.

 _lppszExplicitClass_
  
> [out] Pointeur vers un pointeur vers la classe de message qui définit explicitement comme dossier de réception le dossier vers lequel _pointe lppEntryID_. Cette classe de message doit être identique à la classe dans le paramètre _lpszMessageClass_ ou à une classe de base de cette classe. La transmission de la valeur NULL indique que le dossier pointé par _lppEntryID_ est le dossier de réception par défaut pour le magasin de messages.

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Le dossier de réception a été retourné avec succès.

## <a name="remarks"></a>Remarques

La méthode **IMsgStore::GetReceiveFolder** obtient l’identificateur d’entrée d’un dossier de réception, un dossier désigné pour recevoir les messages entrants d’une classe de message particulière. Les appelants peuvent spécifier une classe de message ou null dans le paramètre _lpszMessageClass_ . Si _lpszMessageClass_ a la valeur NULL, **GetReceiveFolder** retourne les valeurs suivantes :
  
- Dans _lppszExplicitClass_, nom de la première classe de base de la classe de message pointée par _lpszMessageClass_ qui définit explicitement un dossier de réception.

- Dans _lppEntryID_, identificateur d’entrée du dossier de réception pour la classe de base pointé par le paramètre _lppszExplicitClass_ .

Par exemple, supposons que le dossier de réception de la classe de message **IPM. La note** a été définie sur l’identificateur d’entrée de la boîte de réception et **GetReceiveFolder** est appelé avec le contenu de _lpszMessageClass_ défini sur **IPM. Note. Téléphone**. Si **IPM. Note. Téléphone** n’a pas de dossier de réception explicite, **GetReceiveFolder** retourne l’identificateur d’entrée de la boîte de réception dans _lppEntryID_ et **IPM. Remarque** dans _lppszExplicitClass_.
  
Si le client appelle **GetReceiveFolder** pour une classe de message et n’a pas défini de dossier de réception pour cette classe de message, _lppszExplicitClass_ est soit une chaîne de longueur nulle, une chaîne au format Unicode, soit une chaîne au format ANSI, selon que le client a défini l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ .
  
Un dossier de réception par défaut, obtenu en passant null dans le paramètre _lpszMessageClass_ , existe toujours pour chaque magasin de messages.
  
Un client doit appeler la fonction [MAPIFreeBuffer](mapifreebuffer.md) lorsqu’elle est terminée avec l’identificateur d’entrée retourné dans _lppEntryID_ pour libérer la mémoire qui contient cet identificateur d’entrée. Il doit également appeler **MAPIFreeBuffer** quand il est terminé avec la chaîne de classe de message retournée dans _lppszExplicitClass_ pour libérer la mémoire qui contient cette chaîne.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetInbox  <br/> |MFCMAPI utilise la méthode **IMsgStore::GetReceiveFolder** pour localiser le dossier De boîte de réception. |

## <a name="see-also"></a>Voir aussi

[MAPIFreeBuffer](mapifreebuffer.md)  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)
 [MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)
