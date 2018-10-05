---
title: IMAPIPropOpenProperty
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.OpenProperty
api_type:
- COM
ms.assetid: e400e6cc-4e36-43fc-9304-b688a0a7fd77
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7bf1d6912e44319c36e288cd3870218e8c4e45ff
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395804"
---
# <a name="imapipropopenproperty"></a>IMAPIProp::OpenProperty

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Retourne un pointeur vers une interface qui peut être utilisée pour accéder à une propriété.
  
```cpp
HRESULT OpenProperty(
  ULONG ulPropTag,
  LPCIID lpiid,
  ULONG ulInterfaceOptions,
  ULONG ulFlags,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Paramètres

 _ulPropTag_
  
> [in] La balise de propriété pour la propriété auquel accéder. L’identificateur et le type doivent être inclus dans la balise de propriété.
    
 _lpiid_
  
> [in] Pointeur vers l’identificateur de l’interface à utiliser pour accéder à la propriété. Le paramètre _lpiid_ ne doit pas être **null**.
    
 _ulInterfaceOptions_
  
> [in] Données relatives à l’interface identifié par le paramètre _lpiid_ . 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’accès à la propriété. Les indicateurs suivants peuvent être définis :
    
MAPI_CREATE 
  
> Si la propriété n’existe pas, il doit être créé. Si la propriété n’existe pas, la valeur actuelle de la propriété doit être ignorée. Lorsqu’un appelant définit l’indicateur MAPI_CREATE, il doit également affecter l’indicateur ne.
    
MAPI_DEFERRED_ERRORS 
  
> Permet **OpenProperty** retournée correctement, éventuellement, avant de l’objet est entièrement disponible à l’appelant. Si l’objet n’est pas disponible, l’émission d’un appel d’objet suivantes peut déclencher une erreur. 
    
N' 
  
> Dans ce cas, n’est requise :
    
  - Lors de l’ouverture d’une propriété de flux, tels **IID_IStream**, afin de le modifier.
    
  - Lorsque l’ouverture d’une pièce jointe du message incorporé, tel que [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) ouvert avec **IID_IMessage**, afin de le modifier.
    
 _lppUnk_
  
> [out] Pointeur vers l’interface à utiliser pour l’accès à la propriété demandée.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le pointeur d’interface demandé a été renvoyé avec succès.
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> L’interface demandée n’est pas pris en charge pour cette propriété.
    
MAPI_E_NO_ACCESS 
  
> L’appelant a des autorisations suffisantes pour accéder à la propriété.
    
MAPI_E_NO_SUPPORT 
  
> L’objet ne peut pas fournir l’accès à cette propriété par le biais de l’interface demandée.
    
MAPI_E_NOT_FOUND 
  
> La propriété demandée n’existe pas et MAPI_CREATE n’a pas été défini dans le paramètre _ulFlags_ . 
    
MAPI_E_INVALID_PARAMETER 
  
> Le type de propriété dans la balise est défini sur PT_UNSPECIFIED.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIProp::OpenProperty** permet d’accéder à une propriété via une interface particulière. **OpenProperty** est une alternative aux méthodes [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPIProp::SetProps](imapiprop-setprops.md) . Lorsque vous **GetProps** ou **SetProps** échoue parce que la propriété est trop grande ou trop complexe, appelez **OpenProperty**. **OpenProperty** est généralement utilisé pour accéder aux propriétés de type PT_OBJECT. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Pour accéder aux pièces jointes des messages, ouvrez la propriété **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) avec un identificateur d’interface différents, en fonction du type de pièce jointe. Le tableau suivant indique comment appeler **OpenProperty** pour les différents types de pièces jointes : 
  
|**Type de pièce jointe**|**Identificateur de l’interface à utiliser**|
|:-----|:-----|
|Binary  <br/> |IID_IStream  <br/> |
|String  <br/> |IID_IStream  <br/> |
|Message  <br/> |IID_IMessage  <br/> |
|OLE 2.0  <br/> |IID_IStreamDocfile  <br/> |
   
**IStreamDocfile** est un dérivé de l’interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) basé sur un fichier composé OLE 2.0. **IStreamDocfile** est la meilleure solution pour l’accès aux pièces jointes OLE 2.0 car elle implique le moins de surcharge. Vous pouvez utiliser IID_IStreamDocFile pour ces propriétés qui contiennent des données stockées dans le stockage structuré disponible par le biais de l’interface [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) . 
  
Pour plus d’informations sur l’utilisation de **OpenProperty** avec les pièces jointes, voir la propriété **PR_ATTACH_DATA_OBJ** et [l’ouverture d’une pièce jointe](opening-an-attachment.md).
  
N’utilisez pas le pointeur **IStream** que vous recevez pour appeler la méthode son [Seek](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx) ou [SetSize](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx) sauf si vous utilisez une variable zéro position ou la taille. En outre, ne comptez pas sur la valeur du paramètre de sortie _plibNewPosition_ renvoyé à partir de l’appel de la **méthode Seek** . 
  
Si vous appelez **OpenProperty** pour accéder à une propriété de l’interface **IStream** , utilisez uniquement cette interface pour apporter des modifications. N’essayez pas de mettre à jour de la propriété avec les autres [IMAPIProp : IUnknown](imapipropiunknown.md) méthodes, telles que **SetProps** ou [IMAPIProp::DeleteProps](imapiprop-deleteprops.md). 
  
N’essayez pas d’ouvrir une propriété avec **OpenProperty** plusieurs fois. Les résultats ne sont pas définis, car ils peuvent varier d’un fournisseur. 
  
Si vous devez modifier la propriété ouverture, définissez l’indicateur ne. Si vous n’êtes pas certain que l’objet prend en charge la propriété, mais il devrait, définissez les indicateurs MAPI_CREATE et ne. Chaque fois que MAPI_CREATE est défini, ne doit également être définie.
  
Vous êtes responsable de refonte le pointeur d’interface retourné dans le paramètre _lppUnk_ à celui qui est approprié pour l’interface spécifiée dans le paramètre _lpiid_ . Vous devez également utiliser le pointeur retourné pour appeler la méthode [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) lorsque vous avez terminé avec lui. 
  
Parfois, les indicateurs de la configuration dans le paramètre _ulFlags_ n’est pas suffisant pour indiquer le type d’accès à la propriété est obligatoire. Vous pouvez placer des données supplémentaires, telles que les indicateurs, dans le paramètre _ulInterfaceOptions_ . Ces données sont selon l’interface. Utilisent des interfaces (par exemple, **IStream**) et d’autres pas. Par exemple, lorsque vous ouvrez une propriété modifiée avec **IStream**, définir l’indicateur STGM_WRITE dans le paramètre _ulInterfaceOptions_ outre ne. Lorsque vous ouvrez un tableau à l’aide de l’interface [IMAPITable](imapitableiunknown.md) , vous pouvez définir _ulInterfaceOptions_ sur MAPI_UNICODE pour indiquer si les colonnes de la table contenant les propriétés de type chaîne doivent être au format Unicode. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|StreamEditor.cpp  <br/> |CStreamEditor::ReadTextStreamFromProperty  <br/> |MFCMAPI utilise la méthode **IMAPIProp::OpenProperty** pour récupérer une interface de flux de texte de grande taille et propriétés binaires.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [HrIStorageFromStream](hristoragefromstream.md) 
- [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [IMAPIProp::SetProps](imapiprop-setprops.md)
- [IMAPISupport::IStorageFromStream](imapisupport-istoragefromstream.md)
- [IMAPITable : IUnknown](imapitableiunknown.md)
- [IMAPIProp : IUnknown](imapipropiunknown.md)
- [MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)
- [Ouverture d’une pièce jointe](opening-an-attachment.md)

