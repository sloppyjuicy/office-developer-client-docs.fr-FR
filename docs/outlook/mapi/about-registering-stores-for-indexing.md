---
title: À propos de l’inscription de magasins pour l’indexation
description: Décrit comment inscrire des magasins pour l’indexation dans recherche instantanée qui se trouve dans Microsoft Office Outlook.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
ms.openlocfilehash: 3841c490a39fbda17f303034c6e12a27053e78b7
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770263"
---
# <a name="about-registering-stores-for-indexing"></a>À propos de l’inscription de magasins pour l’indexation

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique est spécifique à la recherche instantanée dans Microsoft Office Outlook 2007.
  
La recherche instantanée vous permet de trouver rapidement des éléments dans Outlook. Il utilise des composants de Windows Desktop Search.
  
Le gestionnaire de protocole MAPI vérifie le registre Windows pour les magasins qu’il doit indexer à des fins de recherche. Les fournisseurs de magasins qui souhaitent être indexés doivent être inscrits dans le registre Windows.
  
Par défaut, Windows Desktop Search ajoute les quatre types suivants de fournisseurs de magasins au registre Windows pour autoriser l’indexation :
  
- Stocker les fichiers Dossiers personnels (. PST).
    
-  Microsoft Exchange store, y compris tous les fichiers dossier hors connexion (.ost). 
    
-  Stocker pour les dossiers publics. 
    
-  Stocker pour Microsoft Office Outlook Connecteur pour MSN. 
    
 Les fournisseurs de magasins tiers qui souhaitent être indexés doivent s’inscrire eux-mêmes dans le registre Windows. 
  
> [!NOTE]
> Les administrateurs et les utilisateurs peuvent utiliser un paramètre stratégie de groupe pour empêcher Windows Desktop Search d’indexer Outlook éléments. Pour plus d’informations, consultez [Extending Windows Desktop Search](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx). 
  
## <a name="registry-keys"></a>Clés de Registre

Sur un ordinateur, tous les fournisseurs de magasins qui souhaitent être indexés doivent être inscrits sous une seule des trois clés de Registre suivantes dans le registre Windows. Le gestionnaire de protocole MAPI examine chacune de ces clés dans l’ordre suivant :
  
1. [HKLM]\Software\Policies\Microsoft\Windows\Windows Search\
    
2. [HKLM]\Software\Microsoft\Windows\Windows Search\Preferences\
    
3. [HKCU]\Software\Microsoft\Windows\Windows Search\Preferences\
    
 Chaque valeur sous la clé correspond à un fournisseur de magasin qui serait indexé. Le nom de la valeur est l’identificateur global unique (GUID) du fournisseur de magasin, qui est de type **DWORD** et a la valeur hexadécimale 0x00000001. 
  
## <a name="guids-for-store-providers"></a>GUID pour les fournisseurs du Store

La propriété MAPI **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** spécifie le GUID d’un magasin MAPI. Les GUID des fournisseurs de magasins qui Outlook index sont décrits dans le tableau suivant. 
  
|Type de fournisseur store |GUID |Notes |
|:-----|:-----|:-----|
|Fichiers Dossiers personnels (. PST)  <br/> |{4154494E-BFF9-01B8-00AA-0037D96E0000}  <br/> |Le GUID est documenté dans le fichier d’en-tête public mspst.h en tant que **MSPST_UID_PROVIDER** <br/> |
|Exchange  <br/> |{C0A19454-7F29-1B10-A587-08002B2A2517}  <br/> |Le GUID est documenté dans le fichier d’en-tête public edkmdb.h sous la forme **pbExchangeProviderPrimaryUserGuid** <br/> |
|Dossiers publics  <br/> |{70fab278-f7af-cd11-9bc8-00aa002fc45a}  <br/> |Le GUID est documenté dans le fichier d’en-tête public edkmdb.h sous **la forme pbExchangeProviderPublicGuid** <br/> |
|connecteur Outlook pour MSN  <br/> |{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}  <br/> |Aucun  <br/> |
   
## <a name="see-also"></a>Voir aussi



[À propos de l’API de magasin](about-the-store-api.md)

