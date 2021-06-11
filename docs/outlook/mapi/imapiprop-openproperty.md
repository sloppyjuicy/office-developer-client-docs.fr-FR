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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319809"
---
# <a name="imapipropopenproperty"></a>IMAPIProp::OpenProperty

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie un pointeur vers une interface qui peut être utilisée pour accéder à une propriété.
  
```cpp
HRESULT OpenProperty(
  ULONG ulPropTag,
  LPCIID lpiid,
  ULONG ulInterfaceOptions,
  ULONG ulFlags,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parameters

 _ulPropTag_
  
> [in] Balise de propriété de la propriété à accéder. L’identificateur et le type doivent être inclus dans la balise de propriété.
    
 _lpiid_
  
> [in] Pointeur vers l’identificateur de l’interface à utiliser pour accéder à la propriété. Le  _paramètre lpiid_ ne doit pas être **null**.
    
 _ulInterfaceOptions_
  
> [in] Données liées à l’interface identifiée par _le paramètre lpiid._ 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’accès à la propriété. Les indicateurs suivants peuvent être définies :
    
MAPI_CREATE 
  
> Si la propriété n’existe pas, elle doit être créée. Si la propriété existe, la valeur actuelle de la propriété doit être ignorée. Lorsqu’un appelant définit l’MAPI_CREATE, il doit également définir l’MAPI_MODIFY’indicateur.
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **OpenProperty de** renvoyer correctement, éventuellement avant que l’objet soit entièrement disponible pour l’appelant. Si l’objet n’est pas disponible, effectuer un appel d’objet ultérieur peut occasioner une erreur. 
    
MAPI_MODIFY 
  
> MAPI_MODIFY est nécessaire dans les situations ci-après :
    
  - Lors de l’ouverture d’une propriété de **flux, IID_IStream**, pour la modifier.
    
  - Lors de l’ouverture d’une pièce jointe de message incorporée, [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) ouverte avec **IID_IMessage,** pour la modifier.
    
 _lppUnk_
  
> [out] Pointeur vers l’interface demandée à utiliser pour l’accès aux propriétés.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le pointeur d’interface demandé a été renvoyé avec succès.
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> L’interface demandée n’est pas prise en charge pour cette propriété.
    
MAPI_E_NO_ACCESS 
  
> L’appelant ne dispose pas des autorisations suffisantes pour accéder à la propriété.
    
MAPI_E_NO_SUPPORT 
  
> L’objet ne peut pas fournir l’accès à cette propriété via l’interface demandée.
    
MAPI_E_NOT_FOUND 
  
> La propriété demandée n’existe pas et MAPI_CREATE n’a pas été définie dans le _paramètre ulFlags._ 
    
MAPI_E_INVALID_PARAMETER 
  
> Le type de propriété dans la balise est PT_UNSPECIFIED.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPIProp::OpenProperty** permet d’accéder à une propriété via une interface particulière. **OpenProperty** est une alternative aux méthodes [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPIProp::SetProps.](imapiprop-setprops.md) Lorsque **GetProps ou** **SetProps échoue** parce que la propriété est trop grande ou trop complexe, appelez **OpenProperty**. **OpenProperty est** généralement utilisé pour accéder aux propriétés de type PT_OBJECT. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour accéder aux pièces jointes des messages, ouvrez la propriété **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) avec un identificateur d’interface différent, en fonction du type de pièce jointe. Le tableau suivant décrit comment appeler **OpenProperty** pour les différents types de pièces jointes : 
  
|**Type de pièce jointe**|**Identificateur d’interface à utiliser**|
|:-----|:-----|
|Binaire  <br/> |IID_IStream  <br/> |
|String  <br/> |IID_IStream  <br/> |
|Message  <br/> |IID_IMessage  <br/> |
|OLE 2.0  <br/> |IID_IStreamDocfile  <br/> |
   
**IStreamDocfile est** une dérivée de l’interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) basée sur un fichier composé OLE 2.0. **IStreamDocfile** est le meilleur choix pour accéder aux pièces jointes OLE 2.0, car il implique la charge de travail la moins importante. Vous pouvez utiliser IID_IStreamDocFile pour les propriétés qui contiennent des données stockées dans un stockage structuré disponible via l’interface [IStorage.](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) 
  
Pour plus d’informations sur l’utilisation **d’OpenProperty** avec des pièces jointes, voir la **propriété PR_ATTACH_DATA_OBJ** et [l’ouverture d’une pièce jointe.](opening-an-attachment.md)
  
N’utilisez pas le pointeur **IStream** que vous recevez pour appeler sa méthode [Seek](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx) ou [SetSize,](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx) sauf si vous utilisez une variable de position ou de taille nulle. En outre, ne vous appuyez pas sur la valeur du paramètre de sortie _plibNewPosition_ renvoyée par **l’appel Seek.** 
  
Si vous appelez **OpenProperty** pour accéder à une propriété avec l’interface **IStream,** utilisez uniquement cette interface pour y apporter des modifications. N’essayez pas de mettre à jour la propriété avec les autres méthodes [IMAPIProp : IUnknown,](imapipropiunknown.md) telles que **SetProps** ou [IMAPIProp::D eleteProps](imapiprop-deleteprops.md). 
  
N’essayez pas d’ouvrir une propriété avec **OpenProperty** plusieurs fois. Les résultats ne sont pas indéfinis, car ils peuvent varier d’un fournisseur à l’autre. 
  
Si vous avez besoin de modifier la propriété à ouvrir, définissez l’MAPI_MODIFY’indicateur. Si vous ne savez pas si l’objet prend en charge la propriété, mais vous pensez qu’elle le devrait, définissez les MAPI_CREATE et MAPI_MODIFY indicateurs. Chaque MAPI_CREATE est définie, MAPI_MODIFY doit également être définie.
  
Vous êtes responsable de la rediffusion du pointeur d’interface renvoyé dans le paramètre _lppUnk_ à un pointeur approprié pour l’interface spécifiée dans le _paramètre lpiid._ Vous devez également utiliser le pointeur renvoyé pour appeler sa méthode [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) lorsque vous en avez terminé. 
  
Parfois, la définition des indicateurs dans le  _paramètre ulFlags_ n’est pas suffisante pour indiquer le type d’accès à la propriété qui est requis. Vous pouvez placer des données supplémentaires, telles que des indicateurs, dans le _paramètre ulInterfaceOptions._ Ces données dépendent de l’interface. Certaines interfaces (telles que **IStream)** l’utilisent, tandis que d’autres ne l’utilisent pas. Par exemple, lorsque vous ouvrez une propriété à modifier avec **IStream,** définissez l’indicateur STGM_WRITE dans le paramètre  _ulInterfaceOptions_ en plus de MAPI_MODIFY. Lorsque vous ouvrez un tableau à l’aide de l’interface [IMAPITable,](imapitableiunknown.md) vous pouvez définir  _ulInterfaceOptions_ sur MAPI_UNICODE pour indiquer si les colonnes du tableau qui détiennent des propriétés de chaîne doivent être au format Unicode. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|StreamEditor.cpp  <br/> |CStreamEditor::ReadTextStreamFromProperty  <br/> |MFCMAPI utilise la **méthode IMAPIProp::OpenProperty** pour récupérer une interface de flux pour les propriétés binaires et de texte de grande taille.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [HrIStorageFromStream](hristoragefromstream.md) 
- [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [IMAPIProp::SetProps](imapiprop-setprops.md)
- [IMAPISupport::IStorageFromStream](imapisupport-istoragefromstream.md)
- [IMAPITable : IUnknown](imapitableiunknown.md)
- [IMAPIProp : IUnknown](imapipropiunknown.md)
- [MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
- [Ouverture d’une pièce jointe](opening-an-attachment.md)

