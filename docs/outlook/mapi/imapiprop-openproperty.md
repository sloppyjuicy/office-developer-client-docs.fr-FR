---
title: IMAPIPropOpenProperty
description: Décrit la syntaxe, les paramètres et la valeur de retour d’IMAPIPropOpenProperty, qui retourne un pointeur vers une interface qui peut être utilisée pour accéder à une propriété.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.OpenProperty
api_type:
- COM
ms.assetid: e400e6cc-4e36-43fc-9304-b688a0a7fd77
ms.openlocfilehash: 0665617ca20f5fa59ec5c98b61bd57b45445c835
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816597"
---
# <a name="imapipropopenproperty"></a>IMAPIProp::OpenProperty

**S’applique à** : Outlook 2013 | Outlook 2016 
  
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
  
> [in] Balise de propriété pour la propriété à accéder. L’identificateur et le type doivent être inclus dans la balise de propriété.
    
 _lpiid_
  
> [in] Pointeur vers l’identificateur de l’interface à utiliser pour accéder à la propriété. Le paramètre  _lpiid_ ne doit pas être **null**.
    
 _ulInterfaceOptions_
  
> [in] Données liées à l’interface identifiée par le paramètre  _lpiid_ . 
    
 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle l’accès à la propriété. Les indicateurs suivants peuvent être définis :
    
MAPI_CREATE 
  
> Si la propriété n’existe pas, elle doit être créée. Si la propriété existe, la valeur actuelle de la propriété doit être ignorée. Lorsqu’un appelant définit l’indicateur de MAPI_CREATE, il doit également définir l’indicateur de MAPI_MODIFY.
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **OpenProperty** de retourner correctement, éventuellement avant que l’objet soit entièrement disponible pour l’appelant. Si l’objet n’est pas disponible, l’exécution d’un appel d’objet suivant peut générer une erreur. 
    
MAPI_MODIFY 
  
> MAPI_MODIFY est nécessaire dans les cas suivants :
    
  - Lors de l’ouverture d’une propriété de flux, telle que **IID_IStream**, pour la modifier.
    
  - Lors de l’ouverture d’une pièce jointe de message incorporée, telle que [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) ouverte avec **IID_IMessage**, pour la modifier.
    
 _lppUnk_
  
> [out] Pointeur vers l’interface demandée à utiliser pour l’accès aux propriétés.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le pointeur d’interface demandé a été retourné avec succès.
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> L’interface demandée n’est pas prise en charge pour cette propriété.
    
MAPI_E_NO_ACCESS 
  
> L’appelant dispose d’autorisations insuffisantes pour accéder à la propriété.
    
MAPI_E_NO_SUPPORT 
  
> L’objet ne peut pas fournir l’accès à cette propriété via l’interface demandée.
    
MAPI_E_NOT_FOUND 
  
> La propriété demandée n’existe pas et MAPI_CREATE n’a pas été définie dans le paramètre _ulFlags_ . 
    
MAPI_E_INVALID_PARAMETER 
  
> Le type de propriété dans la balise est défini sur PT_UNSPECIFIED.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIProp::OpenProperty** permet d’accéder à une propriété via une interface particulière. **OpenProperty** est une alternative aux méthodes [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPIProp::SetProps](imapiprop-setprops.md) . Lorsque **GetProps** ou **SetProps** échoue parce que la propriété est trop grande ou trop complexe, appelez **OpenProperty**. **OpenProperty** est généralement utilisé pour accéder aux propriétés de type PT_OBJECT. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour accéder aux pièces jointes de message, ouvrez la propriété **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) avec un identificateur d’interface différent, en fonction du type de pièce jointe. Le tableau suivant décrit comment appeler **OpenProperty** pour les différents types de pièces jointes : 
  
|**Type de pièce jointe**|**Identificateur d’interface à utiliser**|
|:-----|:-----|
|Binary  <br/> |IID_IStream  <br/> |
|Chaîne  <br/> |IID_IStream  <br/> |
|Message  <br/> |IID_IMessage  <br/> |
|OLE 2.0  <br/> |IID_IStreamDocfile  <br/> |
   
**IStreamDocfile** est un dérivé de l’interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) qui est basé sur un fichier composé OLE 2.0. **IStreamDocfile** est le meilleur choix pour accéder aux pièces jointes OLE 2.0, car il implique le moins de surcharge. Vous pouvez utiliser IID_IStreamDocFile pour les propriétés qui contiennent des données stockées dans un stockage structuré disponible via l’interface [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) . 
  
Pour plus d’informations sur l’utilisation **d’OpenProperty** avec des pièces jointes, consultez la propriété **PR_ATTACH_DATA_OBJ** et [l’ouverture d’une pièce jointe](opening-an-attachment.md).
  
N’utilisez pas le pointeur **IStream** que vous recevez pour appeler sa méthode [Seek](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx) ou [SetSize](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx) , sauf si vous utilisez une variable de position ou de taille nulle. En outre, ne vous fiez pas à la valeur du paramètre de sortie  _plibNewPosition_ retourné à partir de l’appel **Seek** . 
  
Si vous appelez **OpenProperty** pour accéder à une propriété avec l’interface **IStream** , utilisez uniquement cette interface pour y apporter des modifications. N’essayez pas de mettre à jour la propriété avec les autres méthodes [IMAPIProp : IUnknown](imapipropiunknown.md) , telles que **SetProps** ou [IMAPIProp::D eleteProps](imapiprop-deleteprops.md). 
  
N’essayez pas d’ouvrir une propriété avec **OpenProperty** plusieurs fois. Les résultats ne sont pas définis, car ils peuvent varier d’un fournisseur à l’autre. 
  
Si vous devez modifier la propriété à ouvrir, définissez l’indicateur MAPI_MODIFY. Si vous ne savez pas si l’objet prend en charge la propriété, mais que vous le pensez, définissez les indicateurs MAPI_CREATE et MAPI_MODIFY. Chaque fois que MAPI_CREATE est défini, MAPI_MODIFY doit également être défini.
  
Vous êtes responsable de la retransformation du pointeur d’interface retourné dans le paramètre _lppUnk_ vers un point approprié pour l’interface spécifiée dans le paramètre _lpiid_ . Vous devez également utiliser le pointeur retourné pour appeler sa méthode [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) lorsque vous en avez terminé avec elle. 
  
Parfois, la définition des indicateurs dans le paramètre _ulFlags_ ne suffit pas à indiquer le type d’accès à la propriété qui est requis. Vous pouvez placer des données supplémentaires, telles que des indicateurs, dans le paramètre _ulInterfaceOptions_ . Ces données dépendent de l’interface. Certaines interfaces (comme **IStream**) l’utilisent, et d’autres non. Par exemple, lorsque vous ouvrez une propriété à modifier avec **IStream**, définissez l’indicateur STGM_WRITE dans le paramètre _ulInterfaceOptions_ en plus de MAPI_MODIFY. Lorsque vous ouvrez une table à l’aide de l’interface [IMAPITable](imapitableiunknown.md) , vous pouvez définir  _ulInterfaceOptions_ sur MAPI_UNICODE pour indiquer si les colonnes de la table qui contiennent des propriétés de chaîne doivent être au format Unicode. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|StreamEditor.cpp  <br/> |CStreamEditor::ReadTextStreamFromProperty  <br/> |MFCMAPI utilise la méthode **IMAPIProp::OpenProperty** pour récupérer une interface de flux pour les propriétés binaires et de texte volumineux. |
   
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

