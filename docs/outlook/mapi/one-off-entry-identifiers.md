---
title: Identificateurs d’entrée unique
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 741d21ae-f14a-4b7f-80aa-91d0f0ff3f34
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 1335de3c1decf6c594f0148fbbf055061d7ce7e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784916"
---
# <a name="one-off-entry-identifiers"></a>Identificateurs d’entrée unique
  
**S’applique à**: Outlook 
  
Identificateurs d’entrée uniques sont créés par MAPI dans la méthode **IAddrBook::CreateOneOff** et par les composants qui n’ont pas accès au sous-système MAPI, tels que des composants de la passerelle. For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md). L’illustration suivante montre le format d’un identificateur d’entrée unique.
  
**Format d’identificateur d’entrée unique**
  
![Format d’identificateur d’entrée unique] (media/amapi_69.gif "Format d’identificateur d’entrée unique")
  
Le premier champ est une structure [MAPIUID](mapiuid.md) spéciale qui identifie l’identificateur d’entrée qui représente un destinataire personnalisé. Cette structure **MAPIUID** doit être définie à la constante MAPI_ONE_OFF_UID. MAPI_ONE_OFF_UID est défini dans le fichier d’en-tête MAPIDEFS. H. 
  
Les champs de version et les indicateurs sont des mots dans l’ordre des octets Intel 16 bits. Le champ version doit être défini sur zéro. Le champ Indicateurs peut avoir les valeurs suivantes :
  
MAPI_ONE_OFF_NO_RICH_INFO
  
MAPI_ONE_OFF_UNICODE
  
L’indicateur MAPI_ONE_OFF_NO_RICH_INFO est défini si un destinataire ne doit pas recevoir le contenu de message dans la Neutral Encapsulation Format TNEF (Transport). Cet indicateur est défini lorsque MAPI_SEND_NO_RICH_INFO est transmis à la méthode [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) . 
  
L’indicateur MAPI_ONE_OFF_UNICODE est défini si l’affichage nom et adresse e-mail est des chaînes Unicode. Cet indicateur est défini lorsque le MAPI_UNICODE est transmis à **IAddrBook::CreateOneOff**. Lorsque l’indicateur MAPI_UNICODE n’est pas transmis à **CreateOneOff**, MAPI suppose que les chaînes d’adresse e-mail et le nom complet dans le jeu de caractères ANSI en cours de la station de travail. En règle générale, les chaînes ANSI ne fonctionnent pas correctement dans les messages envoyés entre plateformes à l’aide de différents jeux de caractères, car la page de codes n’est pas codée dans l’identificateur d’entrée. Pour vous protéger contre cette incompatibilité potentielle, de types d’adresses sont limitées à que les caractères qui sont communes à plusieurs jeux de caractères. Toutefois, pour garantir la compatibilité de plate-forme et le jeu de caractères, les clients doivent utiliser Unicode pour les chaînes de caractères dans leurs messages.
  
Le nom complet est une chaîne qui correspond à la propriété du destinataire **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) et le paramètre de _caractère_ transmis à **IAddrBook::CreateOneOff**. Le jeu de caractères est Unicode si l’indicateur MAPI_ONE_OFF_UNICODE est set et ANSI si elle est désactivée. 
  
Le type d’adresse est une chaîne qui correspond à la propriété du destinataire **TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) et au paramètre _lpszAdrType_ transmis à **IAddrBook::CreateOneOff**. 
  
L’adresse de messagerie est une chaîne qui correspond à la propriété du destinataire **ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) et au paramètre _lpszAddress_ transmis à **IAddrBook::CreateOneOff**. 
  
> [!NOTE]
> Il n’existe pas de remplissage dans les structures d’identificateur d’entrée unique ; les octets sont emballées exactement comme indiqué ci-dessus, la longueur identificateur d’entrée ne doit pas inclure les octets au-delà du caractère null de fin de l’adresse de messagerie. 
  
Clients et fournisseurs de carnet d’adresses qui construire manuellement les identificateurs d’entrée unique devront également générer des valeurs des propriétés de **clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) et **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)). La clé d’enregistrement est identique à l’identificateur d’entrée. La clé de recherche doit être formée par concaténation les champs suivants dans l’ordre suivant :
  
1. Le type d’adresse, converti en majuscules.
    
2. Un signe deux-points ( :)).
    
3. L’adresse de messagerie, convertie en majuscules.
    
4. Un caractère null de fin.
    
Aucune conversion de jeu de caractères ne doit être effectuée lors de la génération de la clé de recherche.
  

