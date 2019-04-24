---
title: OpenIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OpenIMsgOnIStg
api_type:
- HeaderDef
ms.assetid: a98b0b26-9b19-44ca-9b4e-0ad4d1c54325
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6d5ed20e532f0893757cc46d9ea478c7b65acc86
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348614"
---
# <a name="openimsgonistg"></a>OpenIMsgOnIStg

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un nouvel objet [IMessage](imessageimapiprop.md) sur un objet OLE **IStorage** existant, à utiliser dans une session de message. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |IMessage. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
SCODE OpenIMsgOnIStg(
  LPMSGSESS lpMsgSess,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  LPMALLOC lpmalloc,
  LPVOID lpMapiSup,
  LPSTORAGE lpStg,
  MSGCALLRELEASE FAR * lpfMsgCallRelease,
  ULONG ulCallerData,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMsg
);
```

## <a name="parameters"></a>Paramètres

_lpMsgSess_
  
> dans Pointeur vers un objet session de message dans lequel le nouvel objet **IMessage**-sur- **IStorage** doit être créé. 
    
_lpAllocateBuffer_
  
> dans Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) à utiliser pour allouer de la mémoire. 
    
_lpAllocateMore_
  
> dans Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) à utiliser pour allouer de la mémoire supplémentaire. 
    
_lpFreeBuffer_
  
> dans Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) à utiliser pour libérer de la mémoire. 
    
_lpMalloc_
  
> dans Pointeur vers un objet de l'allocation de mémoire qui expose **** l'interface OLE imalloc. L'interface **IMessage** doit utiliser cette méthode d'allocation lorsque vous utilisez des interfaces telles que **IStorage** et **IStream**. 
    
_lpMapiSup_
  
> dans Pointeur facultatif vers un objet de prise en charge MAPI qu'un fournisseur de services peut utiliser pour appeler les méthodes de l'interface [IMAPISupport: IUnknown](imapisupportiunknown.md) . 
    
_lpStg_
  
> [in, out] Pointeur vers un objet **ISTORAGE** OLE ouvert et disposant d'une autorisation en lecture seule ou en lecture/écriture. Étant donné que **IMessage** ne prend pas en charge l'accès en écriture seule, **OpenIMsgOnIStg** n'accepte pas un objet de stockage ouvert en mode écriture seule. 
    
_lpfMsgCallRelease_
  
> dans Pointeur facultatif vers une fonction de rappel basée sur le prototype [MSGCALLRELEASE](msgcallrelease.md) que MAPI doit appeler à la suite de la dernière publication sur l'objet **IMessage**-on- **IStorage** . 
    
_ulCallerData_
  
> dans Données de l'appelant enregistrées par MAPI avec l'objet **IMessage**-sur- **IStorage** et transmises à la fonction de rappel basée sur **MSGCALLRELEASE** . Les données fournissent un contexte sur l'objet **IMessage** en cours de publication et sur l'objet **IStorage** sur lequel il a été créé. 
    
_ulFlags_
  
> dans Masque de des indicateurs utilisé pour contrôler si la méthode OLE **IStorage:: Commit** est appelée lorsque l'application cliente ou le fournisseur de services appelle la méthode **IMessage:: SaveChanges** . Les indicateurs suivants peuvent être définis: 
    
IMSG_NO_ISTG_COMMIT 
  
> La méthode OLE **IStorage:: Commit** ne doit pas être appelée lorsque le client ou le fournisseur appelle [SaveChanges](imapiprop-savechanges.md). 
    
MAPI_UNICODE
  
> Active la création de fichiers. MSG Unicode. Le fichier [IMessage](imessageimapiprop.md) obtenu affiche STORE_UNICODE_OK dans son [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) et prend en charge les propriétés Unicode. 
    
  > [!NOTE]
  > L'indicateur MAPI_UNICODE est pris en charge uniquement dans cette fonction sur Outlook 2003 ou version ultérieure. 
  
_lppMsg_
  
> remarquer Pointeur vers un pointeur vers l'objet **IMessage** ouvert. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les attributs de propriété ne sont accessibles que sur les objets Property, c'est-à-dire les objets qui implémentent l'interface [IMAPIProp: IUnknown](imapipropiunknown.md) . Pour que les propriétés MAPI soient disponibles sur un objet de stockage structuré OLE, **OpenIMsgOnIStg** crée un objet [IMessage: IMAPIProp](imessageimapiprop.md) en haut de l'objet OLE **IStorage** . Les attributs de propriété sur ces objets peuvent être définis ou modifiés avec [SetAttribIMsgOnIStg](setattribimsgonistg.md) et récupérés avec [GetAttribIMsgOnIStg](getattribimsgonistg.md). 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Une session de message doit être ouverte avec [OpenIMsgSession](openimsgsession.md) avant l'appel de **OpenIMsgOnIStg** . Fournir un paramètre _lpMsgSess_ valide garantit que le nouveau message est créé dans une session de message afin qu'il soit fermé à la fermeture de la session. Si _lpMsgSess_ a la valeur null, le message est créé indépendamment de toute session de message. Si l'application cliente ou le fournisseur de services qui a créé le message ne le libère pas, ainsi que toutes ses pièces jointes et tables ouvertes, la mémoire est perdue et peut entraîner la fermeture de l'application. 
  
MAPI utilise les fonctions pointées par _lpAllocateBuffer_, _lpAllocateMore_et _lpFreeBuffer_ pour la plupart de l'allocation et de la libération de mémoire, notamment pour allouer de la mémoire aux applications clientes lors de l'appel d'interfaces d'objets comme [IMAPIProp:: GetProps](imapiprop-getprops.md) et [IMAPITable:: QueryRows](imapitable-queryrows.md). Les pointeurs _lpAllocateBuffer_, _lpAllocateMore_et _lpFreeBuffer_ sont facultatifs lorsque la fonction **OpenIMsgOnIStg** est appelée avec un paramètre _lpMapiSup_ valide. 
  
Étant donné qu'il s'agit d'un objet OLE sous-jacent, MAPI doit également utiliser l'allocation de mémoire OLE. Pour plus d'informations sur les objets de stockage structuré OLE et l'allocation de mémoire OLE, consultez la rubrique _OLE Programmer's Reference_. 
  
Si une valeur valide est fournie pour _lpMapiSup_, **IMessage** prend en charge les indicateurs MAPI_DIALOG et ATTACH_DIALOG en appelant la méthode [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) pour fournir une interface utilisateur de progression pour le [IMAPIProp:: CopyTo](imapiprop-copyto.md) et [IMessage::D méthodes eleteattach](imessage-deleteattach.md) . Par ailleurs, la méthode [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) tente de convertir des identificateurs d'entrée à court terme en appel de la méthode [IMAPISupport:: OpenAddressBook](imapisupport-openaddressbook.md) et d'effectuer des appels sur l'objet carnet d'adresses obtenu. Si NULL est passé pour _lpMapiSup_, **IMESSAGE** ignore MAPI_DIALOG et ATTACH_DIALOG et stocke les identificateurs d'entrée à court terme sans conversion. 
  
L'objet **IStorage** vers lequel pointe le paramètre _lpStg_ doit être ouvert dans le mode STGM_READ ou STGM_READWRITE. Si le mode STGM_READWRITE est utilisé, le mode STGM_TRANSACTED doit également être défini. 
  
La fonction de rappel pointée par le paramètre _lpfMsgCallRelease_ est facultative; s'il est fourni, il doit être basé sur le prototype de fonction [MSGCALLRELEASE](msgcallrelease.md) . L'interface **IMessage** l'appelle lorsque le décompte de références de l'objet **IMessage**-sur- **IStorage** est défini sur zéro par le dernier appel à sa méthode **Release** . La fonction de rappel est couramment utilisée pour libérer l'interface **IStorage** sous-jacente. **IMessage** ne tentera pas d'accéder à l'objet **IStorage** désigné par le paramètre _lpStg_ après avoir effectué le rappel. 
  
Certains clients ou fournisseurs peuvent écrire des données supplémentaires dans l'objet **IStorage** au-delà de la date de l'appel de **IMessage** lors de l'appel de la méthode [SaveChanges](imapiprop-savechanges.md) . Le client ou le fournisseur peut utiliser l'indicateur IMSG_NO_ISTG_COMMIT pour empêcher **IMessage** d'appeler la méthode OLE **IStorage:: Commit** lors du traitement d'un appel de **SaveChanges** ; dans ce cas, le client ou le fournisseur doit lui-même valider l'objet **IStorage** lorsque les données supplémentaires sont écrites. Pour faciliter cette opération, l'implémentation de **IMessage** garantit le nom de tous les sous-stockages créés dans l'objet **IStorage** en commençant par la chaîne «_ _», c'est-à-dire avec deux traits de soulignement. Le client ou le fournisseur peut éviter les collisions de noms en conservant les noms de sous-stockage de cet espace de noms. 
  
MAPI ne définit pas le comportement de plusieurs opérations Open effectuées sur un sous-objet d'un message, telles qu'une pièce jointe, un flux ou un message incorporé. MAPI autorise actuellement un sous-objet déjà ouvert à être ouvert une fois de plus, mais MAPI effectue l'opération d'ouverture en incrémentant le nombre de références pour l'objet Open existant et en le renvoyant au client ou fournisseur qui a appelé [IMessage:: OpenAttach ](imessage-openattach.md)ou [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) . Cela signifie que l'accès demandé pour la première opération d'ouverture sur un sous-objet est l'accès fourni pour toutes les opérations d'ouverture suivantes, quel que soit l'accès demandé par les opérations. 
  
La procédure correcte pour placer un message dans une pièce jointe consiste à appeler la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) avec un identificateur d'interface de IID_IMessage. Actuellement, **OpenProperty** prend également en charge la création de pièces jointes de message disponibles directement sur l'interface OLE **IStorage** , c'est-à-dire à l'aide de l'identificateur d'interface IID_IStorage. L'accès **IStorage** est pris en charge pour permettre la mise en place d'un document Microsoft Word dans une pièce jointe sans la convertir vers ou à partir de l'interface OLE **IStream** . Toutefois, **IMessage** peut ne pas se comporter de manière prévisible si **OpenIMsgOnIStg** reçoit un pointeur **IStorage** vers les données de la pièce jointe, puis les objets sont libérés dans un ordre incorrect. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|File. cpp  <br/> |LoadMSGToMessage  <br/> |MFCMAPI utilise la méthode **OpenIMsgOnIStg** pour ouvrir une interface IMessage en haut du. Fichier MSG de sorte que le fichier peut être manipulé avec MAPI.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

