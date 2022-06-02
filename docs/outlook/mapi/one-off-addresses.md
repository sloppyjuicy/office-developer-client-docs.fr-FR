---
title: Adresses ponctuelles
description: Les adresses uniques sont utilisées pour envoyer des messages aux destinataires uniques, destinataires qui n’ont pas d’entrée correspondante dans les conteneurs de carnets d’adresses de la session.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9224c694-b26f-42c7-9404-ee2dd832cfbb
ms.openlocfilehash: abc562dd4ae86cc2745361442aff3ba866da7ddd
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65852410"
---
# <a name="one-off-addresses"></a>Adresses ponctuelles

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les adresses uniques sont utilisées pour envoyer des messages aux destinataires uniques, destinataires qui n’ont pas d’entrée correspondante dans les conteneurs de carnets d’adresses de la session. Les clients peuvent créer des adresses uniques lorsqu’ils ajoutent de nouvelles entrées au carnet d’adresses ou de nouveaux destinataires à la liste des destinataires d’un message sortant. Des adresses uniques peuvent être ajoutées à n’importe quel conteneur modifiable.
  
Pour créer une adresse unique, les clients utilisent un modèle spécial contenant des contrôles de modification pour entrer toutes les informations qui constituent une adresse unique. Les adresses uniques, comme les adresses d’autres types, utilisent un format prédéfini. Le format d’adresse unique est défini par MAPI comme suit :
  
`Display name[Address type:Email address]`
  
Ce format comporte six composants et certaines règles relatives à la citation de caractères. Les composants sont décrits dans le tableau suivant.
  
|**Composant**|**Utilisation**|**Description**|
|:-----|:-----|:-----|
|Nom d’affichage  <br/> |Facultatif  <br/> |S’il n’est pas présent, **IAddrBook::ResolveName** utilise la partie visible de l’adresse e-mail comme nom d’affichage. Peut inclure des espaces vides. Pour plus d’informations, consultez [IAddrBook::ResolveName](iaddrbook-resolvename.md). |
|[  <br/> |Obligatoire  <br/> |Délimite le début des informations de type et d’adresse. |
|]  <br/> |Obligatoire  <br/> |Délimite la fin des informations de type et d’adresse. Si autre chose que l’espace blanc suit ce caractère, l’entrée n’est pas traitée comme un destinataire personnalisé. |
|Type d’adresse  <br/> |Obligatoire  <br/> |Type d’adresse ; mappe à un format d’adresse spécifique. Pour plus d’informations, consultez [Types d’adresses MAPI](mapi-address-types.md). |
|:  <br/> |Obligatoire  <br/> |Sépare le type d’adresse de l’adresse e-mail. |
|Adresse e-mail  <br/> |Obligatoire  <br/> |Adresse du destinataire. Peut inclure des espaces vides. |
   
MAPI utilise des ensembles particuliers de caractères de citation pour permettre aux adresses de contenir des caractères spéciaux tels que des virgules (,), des crochets gauches ([) et des deux-points (:) et certains caractères nontypeables tels que le retour chariot ou le saut de ligne ou tout autre équivalent hexadécimal. Le caractère de citation est la barre oblique inverse (\). Par conséquent, si les clients ou les fournisseurs doivent insérer une barre oblique inverse dans une adresse, ils doivent le précéder avec le caractère de citation (« \\ »).
  
Les clients et les fournisseurs de services peuvent utiliser cette technique de citation dans l’un des champs non fixes et typables. Par exemple, l’entrée suivante se traduit par Bill Lee comme nom d’affichage, MSPEER comme type d’adresse et \\billll\in comme adresse e-mail :
  
`Bill Lee[MSPEER:\\\\billl\in]`

Pour insérer des caractères spéciaux nontypeables, les clients et les fournisseurs de services utilisent un caractère de citation suivi d’un x et de deux chiffres hexadécimals pour représenter leur équivalent hexadécimal. Par exemple, si une adresse a un caractère nontypeable qui équivaut à un retour chariot (\0d) en hexadécimal, un client les entre comme suit :
  
`Fax Recipient[fax:recipient\x0dbuilding\x0doffice\x0d555-1212\x0d]`

**IAddrBook::ResolveName** analyse également automatiquement la plupart des adresses SMTP, en recherchant les adresses au format suivant : 
  
`XXX@YYY.ZZZ`

Bien que tous les formats RFC822 possibles ne soient pas gérés, cette analyse automatique convient à la plupart des utilisateurs. **ResolveName** inclut cette fonctionnalité pour permettre aux utilisateurs d’entrer des adresses SMTP directement dans un message et d’envoyer ce message à l’utilisateur Internet. Les composants XXX, YYY et ZZZ de l’adresse peuvent être un ou plusieurs caractères. Le signe at (@) ne peut pas être inclus dans les composants d’adresse XXX, YYY ou ZZZ, et le composant YYY ne peut pas non plus inclure le point. Étant donné que les caractères suivants sont des caractères spéciaux dans les adresses SMTP, MAPI convertit automatiquement un nom d’affichage contenant ces caractères en adresse unique : 
  
- \>\>
    
- @
    
- \<\>
    
- .
    
Un identificateur d’entrée unique correspondant est attribué à chaque adresse unique. Pour effectuer cette affectation, les clients appellent **IAddrBook::CreateOneOff** et les fournisseurs de transport appellent **IMAPISupport::CreateOneOff**. Pour plus d’informations, consultez [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) et [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md). Lors du traitement des messages entrants, les fournisseurs de transport créent des identificateurs d’entrée uniques pour les adresses de passerelle et pour les adresses qui ne peuvent pas être gérées par les fournisseurs de carnets d’adresses associés au transport. Les fournisseurs de transport vérifient le type de chaque adresse dans un message pour déterminer si elle peut être gérée par un fournisseur de carnet d’adresses associé au transport. Si ce n’est pas le cas, les fournisseurs de transport appellent **IMAPISupport::CreateOneOff** pour associer l’adresse à un identificateur d’entrée unique. 
  
Les identificateurs d’entrée unique incluent les informations suivantes dans l’ordre suivant :
  
1. **MAPIUID**
    
2. Version
    
3. Flags
    
4. Nom
    
5. Type d’adresse
    
6. Adresse e-mail
    
Dans les appels à **IAddrBook::CreateOneOff** et **IMAPISupport::CreateOneOff**, les clients et les fournisseurs de transport peuvent définir un indicateur qui indique si le destinataire représenté par l’adresse unique peut traiter du texte mis en forme ou des objets OLE incorporés. Pour indiquer qu’un destinataire peut gérer le texte mis en forme et les objets OLE, les clients et les fournisseurs de transport définissent l’indicateur MAPI_SEND_NO_RICH_INFO dans le paramètre _ulFlags_ . MAPI définit ensuite la propriété **PR_SEND_RICH_INFO** du destinataire unique ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) sur FALSE. Lorsque cet indicateur n’est pas défini, MAPI définit **PR_SEND_RICH_INFO** sur TRUE, sauf si l’adresse unique est interprétée comme une adresse SMTP. Dans ce cas, **PR_SEND_RICH_INFO** valeur par défaut false. 
  
## <a name="see-also"></a>Voir aussi

- [IAddrBook::ResolveName](iaddrbook-resolvename.md)

