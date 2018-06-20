---
title: IMAPIPropGetIDsFromNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetIDsFromNames
api_type:
- COM
ms.assetid: e3f501a4-a8ee-43d7-bd83-c94e7980c398
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5247ca71c88b9c0f8591a732746a17204265741c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783906"
---
# <a name="imapipropgetidsfromnames"></a>IMAPIProp::GetIDsFromNames

  
  
**S’applique à**: Outlook 
  
Fournit les identificateurs de propriété qui correspondent à un ou plusieurs noms de propriété.
  
```cpp
HRESULT GetIDsFromNames(
  ULONG cPropNames,
  LPMAPINAMEID FAR * lppPropNames,
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTags
);
```

## <a name="parameters"></a>Paramètres

 _cPropNames_
  
> [in] Le nombre de noms de propriété indiqué par le paramètre _lppPropNames_ . Si _lppPropNames_ est NULL, le paramètre _cPropNames_ doit être 0. 
    
 _lppPropNames_
  
> [in] Pointeur vers un tableau de noms de propriété, ou NULL. Transmission NULL demande des identificateurs de propriété pour tous les noms de propriété dans tous les jeux de propriétés sur laquelle l’objet comporte des informations. Le paramètre _lppPropNames_ ne doit pas être NULL si l’indicateur MAPI_CREATE est défini dans le paramètre _ulFlags_ . 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui indique la façon dont les identificateurs de propriété doivent être retournés. Vous pouvez définir l’indicateur suivant :
    
MAPI_CREATE 
  
> Affecte un identificateur de propriété, si une n’a encore été attribuée, à un ou plusieurs noms inclus dans le tableau de noms de propriété désigné par _lppPropNames_. Cet indicateur enregistre en interne l’identificateur dans la table de mappage de nom-à-identificateur.
    
 _lppPropTags_
  
> [out] Pointeur vers un pointeur vers un tableau de balises de propriété qui contient les identificateurs de propriété existant ou nouvellement affecté. Les types de propriétés pour les balises de propriété dans ce tableau sont définis sur **PT_UNSPECIFIED**.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Les identificateurs des noms de propriétés spécifié a été correctement retournés.
    
MAPI_E_NO_SUPPORT 
  
> L’objet ne gère pas les propriétés nommées.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> Mémoire insuffisante n’était disponible pour récupérer les identificateurs.
    
MAPI_E_TOO_BIG 
  
> Impossible d’effectuer l’opération car elle requiert trop de balises de propriété à renvoyer.
    
MAPI_W_ERRORS_RETURNED 
  
> L’appel a réussi, mais un ou plusieurs identificateurs de propriété n’a pas peuvent être retournés. Le type de propriété correspondante pour chaque propriété non disponible est égale à **PT_ERROR** et son identificateur à zéro. Lorsque cet avertissement est renvoyé, gérer l’appel comme réussie. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Consultez [utilisation de Macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIProp::GetIDsFromNames** récupère un tableau de balises de propriété qui contiennent les identificateurs de propriété pour un ou plusieurs des propriétés nommées. **IMAPIProp::GetIDsFromNames** peut être appelée pour effectuer les opérations suivantes : 
  
- Créer des identificateurs pour les nouveaux noms.
    
- Récupérer les identificateurs de noms spécifiques.
    
- Récupérer les identificateurs de toutes les propriétés nommées qui sont incluses dans le mappage de l’objet.
    
Propriétés nommées sont généralement utilisées par les fournisseurs de banque de messages pour les dossiers et messages. Autres objets, tels que les utilisateurs et aux sections de profil de messagerie ne peuvent pas prendre en charge l’association des noms pour les identificateurs de propriété et peuvent retourner des MAPI_E_NO_SUPPORT de **GetIDsFromNames**.
  
S’il existe une erreur qui renvoie un identificateur pour un nom donné, **GetIDsFromNames** renvoie MAPI_W_ERRORS_RETURNED et définit le type de propriété dans l’entrée de tableau de balise de propriété qui correspond au nom **PT_ERROR** et l’identificateur de zéro. 
  
Mappage de nom à identificateur est représenté par la propriété **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) d’un objet. **PR_MAPPING_SIGNATURE** contient une structure [MAPIUID](mapiuid.md) qui indique le responsable de l’objet de fournisseur de services. Si la propriété **PR_MAPPING_SIGNATURE** est le même pour les deux objets, supposent que ces objets utilisent le même mappage à-identificateur de nom. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Les identificateurs que vous passez dans le tableau de balise de propriété indiqué par le paramètre _lppPropNames_ doivent être dans la plage 0 x 8000 à 0xFFFE. Les entrées de ce tableau doivent être dans le même ordre que les noms transmis dans le tableau de la propriété nom désignées par _lppPropNames_. 
  
Si vous prenez en charge les propriétés nommées dans un conteneur, utilisez le mappage de nom-identificateur de même pour tous les objets dans le conteneur (autrement dit, n’utilisez pas un autre mappage pour chaque dossier de la banque de messages ou de chaque message dans le dossier).
  
## <a name="notes-to-callers"></a>Notes aux appelants

Étant donné que les types de propriétés pour les identificateurs de tableau de la propriété tag désignés par _lppPropTags_ renvoyées sont définis sur **PT_UNSPECIFIED**, vous devez appeler la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) pour récupérer les types précis. 
  
Si vous déplacez ou copier des objets avec des propriétés nommées et les objets source et de destination ont des signatures différentes mappage telle qu’indiquée par les valeurs de leurs propriétés **PR_MAPPING_SIGNATURE** , vous devez conserver les noms pendant ces opérations. Pour conserver les noms de propriété, ajustez les identificateurs de propriété correspondante pour correspondre au mappage à-identificateur de nom de l’objet de destination. 
  
Certains objets ont une limite pour le nombre d’identificateurs de propriété que peuvent de nom. Si un appel à **GetIDsFromNames** provoque le dépassement de cette limite, la méthode renvoie MAPI_E_TOO_BIG. Dans ce cas, des requêtes par identificateur. 
  
Pour plus d’informations, voir [Les propriétés MAPI nommée](mapi-named-properties.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::FindAllNamedPropsUsed  <br/> |MFCMAPI utilise la méthode **IMAPIProp::GetIDsFromNames** pour obtenir les balises de propriété pour toutes les propriétés nommées qui ont été mappées.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[MAPINAMEID](mapinameid.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[MAPI des propri�t�s nomm�e](mapi-named-properties.md)
  
[Utilisation de Macros pour la gestion des erreurs](using-macros-for-error-handling.md)

