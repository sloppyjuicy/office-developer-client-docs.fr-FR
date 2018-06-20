---
title: Adresses uniques
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9224c694-b26f-42c7-9404-ee2dd832cfbb
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 598ced18d659fcbe52ded07cc3bb80dc396eddbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784937"
---
# <a name="one-off-addresses"></a>Adresses uniques

**S’applique à**: Outlook 
  
Adresses uniques sont utilisées pour envoyer des messages aux destinataires uniques, les destinataires qui n’ont pas d’entrée correspondante dans les conteneurs de carnet d’adresses de la session. Les clients peuvent créer des adresses uniques lorsqu’ils ajoutent de nouvelles entrées pour le carnet d’adresses ou les nouveaux destinataires à la liste des destinataires d’un message sortant. Adresses uniques peuvent être ajoutés à n’importe quel conteneur est modifiable.
  
Pour créer une adresse unique, les clients utilisent un modèle spécial contenant des contrôles d’édition pour la saisie de toutes les informations qui constitue une adresse unique. Adresses uniques, comme les adresses d’autres types, utilisent un format prédéfini. Le format d’adresse uniques est défini par MAPI comme suit :
  
`Display name[Address type:Email address]`
  
Il existe six composants dans ce format et certaines règles sur les caractères. Les composants sont décrits dans le tableau suivant.
  
|**Composant**|**Utilisation**|**Description**|
|:-----|:-----|:-----|
|Nom d’affichage  <br/> |Facultatif  <br/> |Le cas contraire, **IAddrBook::ResolveName** utilise la partie visible de l’adresse de messagerie comme nom d’affichage. Peut inclure des espaces. Pour plus d’informations, voir [IAddrBook::ResolveName](iaddrbook-resolvename.md).  <br/> |
|[  <br/> |Obligatoire  <br/> |Représente des informations de type et l’adresse de début.  <br/> |
|]  <br/> |Obligatoire  <br/> |Représente la fin des informations de type et l’adresse. Si l’espace suit ce caractère, l’entrée n’est pas traitée comme un destinataire personnalisé.  <br/> |
|Type d’adresse  <br/> |Obligatoire  <br/> |Type d’adresse ; correspond à un format d’adresse spécifique. Pour plus d’informations, voir [Types d’adresses MAPI](mapi-address-types.md).  <br/> |
|:  <br/> |Obligatoire  <br/> |Sépare le type d’adresse de l’adresse de messagerie.  <br/> |
|Adresse de messagerie  <br/> |Obligatoire  <br/> |Adresse du destinataire. Peut inclure des espaces.  <br/> |
   
MAPI utilise particulier jeux de caractères de citation pour autoriser les adresses contenant des caractères spéciaux tels que des virgules (,), crochet ([]), gauche et deux-points ( :)) et certains caractères tels que le transport insaisissables renvoyer ou ligne flux ou tout autre équivalent hexadécimal. Le caractère indentation est la barre oblique inverse (\). Par conséquent, si les clients ou fournisseurs doivent insérer une barre oblique inverse dans une adresse, ils doivent précédez avec le caractère indentation («\\»).
  
Clients et fournisseurs de services peuvent utiliser cette technique indentation dans les champs nonfixed, à taper. Par exemple, l’entrée suivante se traduit par Bill Lee comme nom d’affichage, MSPEER comme type d’adresse, et \\billll\in en tant que l’adresse de messagerie :
  
`Bill Lee[MSPEER:\\\\billl\in]`

Pour insérer des caractères spéciaux moyenne isolée, clients et fournisseurs de services utilisent un caractère indentation suivi d’un x deux chiffres hexadécimaux pour représenter leur équivalent hexadécimal. Par exemple, si une adresse a un caractère moyenne isolée qui équivaut à un chariot retourner, (\0d) au format hexadécimal, un client en tant qu’entreriez :
  
`Fax Recipient[fax:recipient\x0dbuilding\x0doffice\x0d555-1212\x0d]`

**IAddrBook::ResolveName** analyse automatiquement la plupart des adresses SMTP, recherchez les adresses avec le format suivant : 
  
`XXX@YYY.ZZZ`

Bien que tous les formats RFC822 possibles sont gérés, cette analyse automatique est suffisante pour la plupart des utilisateurs. **ResolveName** inclut cette fonctionnalité pour permettre aux utilisateurs d’entrer des adresses SMTP directement dans un message et que ce message l’utilisateur accède à l’utilisateur d’Internet. Les composants XXX, YYY et ZZZ de l’adresse peuvent être un ou plusieurs caractères. L’arobase (@) ne peut pas être inclus dans la zone Adresse XXX, YYY ou ZZZ composants et le composant YYY également ne peut pas inclure le point. Étant donné que les caractères suivants sont des caractères spéciaux dans les adresses SMTP, MAPI convertit automatiquement un nom d’affichage contenant ces caractères dans une adresse unique : 
  
- \>\>
    
- @
    
- \<\>
    
- .
    
Toutes les adresses uniques sont affecté un identificateur d’entrée unique. Pour rendre cette affectation, les clients appellent **IAddrBook::CreateOneOff** et fournisseurs de transport appelez **IMAPISupport::CreateOneOff**. Pour plus d’informations, voir [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) et [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md). Lors du traitement des messages entrants, fournisseurs de transport créent des identificateurs d’entrée unique pour les adresses de la passerelle et pour les adresses qui ne peuvent pas être gérés par les fournisseurs de carnet d’adresses associé à de transport. Fournisseurs de transport vérifient le type de chaque adresse dans un message afin de déterminer si elle peut être gérée par un fournisseur de carnet d’adresses associé avec le transport. Si elle n’est pas le cas, les fournisseurs de transport appeler **IMAPISupport::CreateOneOff** pour associer l’adresse à un identificateur d’entrée unique. 
  
Identificateurs d’entrée unique incluent les informations suivantes dans l’ordre suivant :
  
1. **MAPIUID**
    
2. Version
    
3. Indicateurs
    
4. Nom d’affichage
    
5. Type d’adresse
    
6. Adresse de messagerie
    
Dans les appels à **IAddrBook::CreateOneOff** et **IMAPISupport::CreateOneOff**, les clients et des fournisseurs de transport peuvent définir un indicateur qui indique si le destinataire représenté par l’adresse unique peut traiter mise en forme de texte ou incorporé OLE objets. Pour indiquer qu’un destinataire peut gérer la mise en forme de texte et aux objets OLE, clients et fournisseurs de transport définir l’indicateur MAPI_SEND_NO_RICH_INFO dans le paramètre _ulFlags_ . MAPI définit l’uniques propriété du destinataire **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) à FALSE. Lorsque cet indicateur n’est pas défini, MAPI définit **PR_SEND_RICH_INFO** sur TRUE, sauf si l’adresse unique est interprétée comme une adresse SMTP. Dans ce cas, **PR_SEND_RICH_INFO** par défaut est FALSE. 
  
## <a name="see-also"></a>Voir aussi

- [IAddrBook::ResolveName](iaddrbook-resolvename.md)

