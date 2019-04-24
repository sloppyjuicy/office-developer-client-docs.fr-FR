---
title: Identificateurs d’entrée ponctuelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 741d21ae-f14a-4b7f-80aa-91d0f0ff3f34
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: abe52cb45e13e6713d28fffe379e245e2483bffa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279690"
---
# <a name="one-off-entry-identifiers"></a>Identificateurs d’entrée ponctuelle
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les identificateurs d'entrée uniques sont créés par MAPI dans la méthode **IAddrBook:: CreateOneOff** et par les composants qui n'ont pas accès au sous-système MAPI, tels que les composants de passerelle. For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md). L'illustration suivante montre le format d'un identificateur d'entrée unique.
  
**Format d’identificateur d’entrée unique**
  
![Format d'identificateur d'entrée unique] (media/amapi_69.gif "Format d'identificateur d'entrée unique")
  
Le premier champ est une structure [MAPIUID](mapiuid.md) spéciale qui identifie l'identificateur d'entrée comme représentant un destinataire personnalisé. Cette structure **MAPIUID** doit être définie sur la constante MAPI_ONE_OFF_UID. MAPI_ONE_OFF_UID est défini dans le fichier d'en-tête MAPIDEFS. H. 
  
Les champs version et Flags sont des mots 16 bits dans l'ordre d'octet Intel. Le champ version doit avoir la valeur zéro. Le champ Flags peut avoir les valeurs suivantes:
  
MAPI_ONE_OFF_NO_RICH_INFO
  
MAPI_ONE_OFF_UNICODE
  
L'indicateur MAPI_ONE_OFF_NO_RICH_INFO est défini si un destinataire ne doit pas recevoir de contenu de message au format TNEF (Transport Neutral Encapsulation Format). Cet indicateur est défini lorsqu'MAPI_SEND_NO_RICH_INFO est transmis à [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) méthode. 
  
L'indicateur MAPI_ONE_OFF_UNICODE est défini si le nom d'affichage et l'adresse de messagerie sont des chaînes Unicode. Cet indicateur est défini lorsque la MAPI_UNICODE est transmise à **IAddrBook:: CreateOneOff**. Lorsque l'indicateur MAPI_UNICODE n'est pas transmis à **CreateOneOff**, MAPI suppose que le nom d'affichage et les chaînes d'adresse de messagerie se trouvent dans le jeu de caractères ANSI actuel de la station de travail. En règle générale, les chaînes ANSI ne fonctionnent pas correctement dans les messages qui sont envoyés entre les plateformes utilisant des jeux de caractères différents car la page de code n'est pas codée dans l'identificateur d'entrée. Pour vous protéger contre cette incompatibilité potentielle, de nombreux types d'adresses sont limités aux seuls caractères communs à plusieurs jeux de caractères. Toutefois, pour garantir la compatibilité des jeux de caractères et des plateformes, les clients doivent utiliser Unicode pour les chaînes de caractères de leurs messages.
  
Le nom complet est une chaîne terminée par un caractère null qui correspond à la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) du destinataire et au paramètre _lpszName_ transmis à **IAddrBook:: CreateOneOff**. Le jeu de caractères est Unicode si l'indicateur MAPI_ONE_OFF_UNICODE est défini et ANSI s'il est clair. 
  
Le type d'adresse est une chaîne terminée par un caractère null qui correspond à la propriété **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) du destinataire et au paramètre _lpszAdrType_ transmis à **IAddrBook:: CreateOneOff**. 
  
L'adresse de messagerie est une chaîne terminée par un caractère null qui correspond à la propriété **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) du destinataire et au paramètre _lpszAddress_ transmis à **IAddrBook:: CreateOneOff**. 
  
> [!NOTE]
> Il n'y a pas de remplissage dans les structures d'identificateur d'entrée unique; les octets sont conditionnés exactement comme indiqué ci-dessus et la longueur de l'identificateur d'entrée ne doit pas inclure d'octets au-delà du caractère null de fin de l'adresse de messagerie. 
  
Les clients et les fournisseurs de carnets d'adresses qui construisent manuellement des identificateurs d'entrée uniques peuvent également avoir besoin de générer des valeurs pour les propriétés **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) et **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). La clé d'enregistrement est identique à l'identificateur d'entrée. La clé de recherche doit être formée en concaténant les champs suivants dans l'ordre suivant:
  
1. Type d'adresse, converti en caractères majuscules.
    
2. Un signe deux-points (:).
    
3. Adresse de messagerie convertie en caractères majuscules.
    
4. Caractère null de fin.
    
Aucune conversion de jeu de caractères ne doit être réalisée lors de la génération de la clé de recherche.
  

