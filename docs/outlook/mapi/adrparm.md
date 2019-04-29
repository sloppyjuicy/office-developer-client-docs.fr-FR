---
title: ADRPARM
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRPARM
api_type:
- COM
ms.assetid: 35cd57b4-9901-456c-bf06-1f84e274eb4e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9663a25a50d914f47cff48124898d16318bbbc43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425896"
---
# <a name="adrparm"></a>ADRPARM

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit l'affichage et le comportement de la boîte de dialogue adresse commune. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _ADRPARM
{
  ULONG cbABContEntryID;
  LPENTRYID lpABContEntryID;
  ULONG ulFlags;
  LPVOID lpReserved;
  ULONG ulHelpContext;
  LPSTR lpszHelpFileName;
  LPFNABSDI lpfnABSDI;
  LPFNDISMISS lpfnDismiss;
  LPVOID lpvDismissContext;
  LPSTR lpszCaption;
  LPSTR lpszNewEntryTitle;
  LPSTR lpszDestWellsTitle;
  ULONG cDestFields;
  ULONG nDestFieldFocus;
  LPSTR FAR *lppszDestTitles;
  ULONG FAR *lpulDestComps;
  LPSRestriction lpContRestriction;
  LPSRestriction lpHierRestriction;
} ADRPARM, FAR *LPADRPARM;

```

## <a name="members"></a>Members

**cbABContEntryID**
  
> Nombre d'octets dans l'identificateur d'entrée pointé par **lpABContEntryID**.
    
**lpABContEntryID**
  
> Pointeur vers l'identificateur d'entrée du conteneur qui fournit la liste initiale des adresses de destinataires qui sont affichées dans la boîte de dialogue d'adresses.
    
**ulFlags**
  
> Masque de des indicateurs associés à différentes options de la boîte de dialogue adresse. Les indicateurs suivants peuvent être définis:
    
AB_RESOLVE
  
> Activer la résolution de tous les noms une fois la boîte de dialogue d'adresses fermée. S'il existe des entrées ambiguës résultant du processus de résolution de noms, une boîte de dialogue s'affiche pour inviter l'utilisateur à le résoudre. La définition de cet indicateur garantit que tous les noms renvoyés par [IAddrBook:: Address](iaddrbook-address.md) sont résolus. 
    
AB_SELECTONLY
  
> Désactive la création d'adresses uniques pour une liste de destinataires. Cet indicateur est utilisé uniquement si la boîte de dialogue est modale, comme indiqué par l'indicateur DIALOG_MODAL défini.
    
ADDRESS_ONE
  
> L'utilisateur peut sélectionner un seul destinataire au lieu de plusieurs destinataires dans une liste. Cet indicateur est valide uniquement lorsque **cDestFields** est égal à zéro et que la boîte de dialogue est modale, comme indiqué par l'indicateur DIALOG_MODAL défini. 
    
DIALOG_MODAL
  
> Entraîne l'affichage de la version modale de la boîte de dialogue d'adresses commune. Cet indicateur ou DIALOG_SDI doit être défini; elles ne peuvent pas être définies à la fois. 
    
DIALOG_OPTIONS
  
> Entraîne l'affichage du bouton **options d'envoi** dans la boîte de dialogue. Cet indicateur est utilisé uniquement si la boîte de dialogue est modale, comme indiqué par l'indicateur DIALOG_MODAL défini. 
    
DIALOG_SDI
  
> Entraîne l'affichage de la version non modale de la boîte de dialogue d'adresses commune. Cet indicateur ou DIALOG_MODAL doit être défini; elles ne peuvent pas être définies à la fois. L'indicateur DIALOG_SDI est ignoré pour les clients non-Outlook et la version modale de la boîte de dialogue s'affiche. Par conséquent, un pointeur vers un descripteur ne doit pas être attendu dans le paramètre _lpulUIParam_ de [IAddrBook:: Address](iaddrbook-address.md).
    
**lpReserved**
  
> Réservé, doit être égal à zéro.
    
**ulHelpContext**
  
> Indique le contexte dans l' **aide** qui s'affichera en premier lorsque l'utilisateur clique sur le bouton aide dans la boîte de dialogue adresse. 
    
**lpszHelpFileName**
  
> Pointeur vers le nom d'un fichier d'aide qui sera associé à la boîte de dialogue d'adresse. Le membre **lpszHelpFileName** est utilisé avec **ulHelpContext** pour appeler la fonction **WinHelp** de Windows. 
    
**lpfnABSDI**
  
> Pointeur vers une fonction MAPI basée sur le prototype [ACCELERATEABSDI](accelerateabsdi.md) ou sur null. Ce membre s'applique uniquement à la version non modale de la boîte de dialogue, comme indiqué par l'indicateur DIALOG_SDI défini. Les clients qui créent une structure **ADRPARM** à transmettre à [IAddrBook:: Address](iaddrbook-address.md) doivent toujours définir le membre **lpfnABSDI** sur null. Si l'indicateur DIALOG_SDI est défini, MAPI le définira sur une fonction valide avant de renvoyer. Les clients appellent cette fonction à partir de dans leur boucle de messages pour s'assurer que les accélérateurs dans la boîte de dialogue Carnet d'adresses fonctionnent. Lorsque la boîte de dialogue est fermée et MAPI appelle la fonction vers laquelle pointe le membre **lpfnDismiss** , les clients doivent déconnecter la fonction **ACCELERATEABSDI** de leur boucle de messages. 
    
**lpfnDismiss**
  
> Pointeur vers une fonction basée sur le prototype [DISMISSMODELESS](dismissmodeless.md) ou sur null. Ce membre s'applique uniquement à la version non modale de la boîte de dialogue uniquement, comme indiqué par l'indicateur DIALOG_SDI défini. MAPI appelle la fonction **DISMISSMODELESS** lorsque l'utilisateur fait disparaître la boîte de dialogue d'adresses non modale, en informant un client appelant **IAddrBook:: Address** que la boîte de dialogue n'est plus active. 
    
**lpvDismissContext**
  
> Pointeur vers les informations de contexte à transmettre à la fonction **DISMISSMODELESS** vers laquelle pointe le membre **lpfnDismiss** . Ce membre s'applique uniquement à la version non modale de la boîte de dialogue, comme indiqué par l'indicateur DIALOG_SDI défini. 
    
**lpszCaption**
  
> Pointeur vers le texte à utiliser comme titre de la boîte de dialogue adresse commune.
    
**lpszNewEntryTitle**
  
> Pointeur vers le texte à utiliser comme étiquette de bouton pour le bouton qui appelle la boîte de dialogue **nouvelle entrée** ou une autre boîte de dialogue. 
    
**lpszDestWellsTitle**
  
> Pointeur vers le texte à utiliser comme titre pour les contrôles de zone de texte de destinataire pouvant apparaître dans la version modale de la boîte de dialogue adresse commune. Ce membre n'est pas utilisé pour les boîtes de dialogue non modales. 
    
**cDestFields**
  
> Nombre de contrôles de zone de texte de destinataire dans la version modale de la boîte de dialogue d'adresses, ou zéro si la boîte de dialogue est non modale. La boîte de dialogue adresse est ouverte pour la navigation uniquement lorsque les conditions suivantes sont vraies: 
    
  - Le membre **cDestFields** est défini sur zéro. 
    
  - L'indicateur DIALOG_BOX est défini.
    
  - L'indicateur ADDRESS_ONE n'est pas défini.
    
  La définition de **cDestFields** sur 0xFFFFFFFF implique que MAPI doit créer le nombre par défaut de contrôles de zone de texte de destinataire. Dans ce cas, les membres **lppszDestTitles** et **LPULDESTCOMPS** doivent être null. 
    
**nDestFieldFocus**
  
> Indique le contrôle de zone de texte qui doit avoir le focus initial lorsque la version modale de la boîte de dialogue s'affiche. Cette valeur doit être comprise entre 0 et la valeur de **cDestFields** moins 1. 
    
**lppszDestTitles**
  
> Pointeur vers un tableau d'étiquettes pour les boutons associés à chacun des contrôles de zone de texte qui sont affichés dans la version modale de la boîte de dialogue d'adresse. La valeur du membre **cDestFields** indique le nombre d'étiquettes incluses dans le tableau. Si le membre **lppszDestTitles** est null, la méthode **Address** utilise les titres par défaut. 
    
**lpulDestComps**
  
> Pointeur vers un tableau de valeurs de type de destinataire, telles que MAPI_TO, MAPI_CC et MAPI_BCC, qui est associé à chaque contrôle de zone de texte. La valeur du membre **CDestFields** indique le nombre de types de destinataires inclus dans le tableau. Les valeurs indiquées par **lpulDestComps** peuvent être utilisées pour définir la propriété **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) de chaque destinataire. Si le membre **lpulDestComps** est null, la méthode **Address** utilise les types de destinataires par défaut. 
    
**lpContRestriction**
  
> Pointeur vers une structure [SRestriction](srestriction.md) qui limite le type d'entrées d'adresse pouvant être affichées dans la boîte de dialogue. 
    
**lpHierRestriction**
  
> Pointeur vers une structure **SRestriction** qui limite les conteneurs de carnet d'adresses pouvant fournir des entrées d'adresse à afficher dans la boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

Les structures **ADRPARM** sont utilisées par les clients et les fournisseurs de services pour contrôler l'apparence et le comportement des boîtes de dialogue d'adresses communes MAPI. Il existe deux sortes de boîte de dialogue d'adresses: non modal et modal. Certains membres de la structure **ADRPARM** s'appliquent aux deux versions de la boîte de dialogue, mais d'autres s'appliquent uniquement à l'une des deux versions. Le tableau suivant lie les membres d'une structure **ADRPARM** à leur utilisation dans les boîtes de dialogue d'adresses communes. 
  
|Membre ADRPARM|Type de boîte de dialogue|
|:-----|:-----|
|**cbABContEntryID** et **lpABContEntryID** <br/> |Modal et non modal  <br/> |
|**ulFlags** <br/> |Modal et non modal  <br/> |
|**lpReserved** <br/> |Modal et non modal  <br/> |
|**ulHelpContext** et **lpszHelpFileName** <br/> |Modal et non modal  <br/> |
|**lpfnABSDI** <br/> |Non modal  <br/> |
|**lpfnDismiss** et **lpvDismissContext** <br/> |Non modal  <br/> |
|**lpszCaption** <br/> |Modal et non modal  <br/> |
|**lpszNewEntryTitle** <br/> |Modal  <br/> |
|**lpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **lppszDestTitles**et **lpulDestComps** <br/> |Modal  <br/> |
|**lpContRestriction** <br/> |Modal et non modal  <br/> |
|**lpHierRestriction** <br/> |Modal et non modal  <br/> |
   
La boîte de dialogue non modale est un affichage en lecture seule d'entrées provenant d'un ou de plusieurs conteneurs de carnet d'adresses. La boîte de dialogue peut afficher toutes les entrées des conteneurs sélectionnés ou se limiter uniquement aux entrées et aux conteneurs correspondant aux critères établis par une restriction. La restriction de contenu pointée par **lpContRestriction** peut limiter les types d'entrées affichés et la restriction de hiérarchie pointée par **lpHierRestriction** peuvent limiter les conteneurs qui fournissent les entrées. Pour informer l'appelant lors de la fermeture de la boîte de dialogue, MAPI appelle une fonction qui est fournie par l'appelant et qui correspond au prototype [DISMISSMODELESS](dismissmodeless.md) . Une autre fonction, qui correspond au prototype [ACCELERATEABSDI](accelerateabsdi.md) , est fournie par MAPI et appelée par l'appelant dans la boucle de messages Windows pour faciliter le travail des raccourcis clavier. La version non modale de la boîte de dialogue adresse MAPI peut être affichée lorsque les clients appellent [IAddrBook:: adresse](iaddrbook-address.md) ou lorsque les fournisseurs de services appellent [IMAPISupport:: adresse](imapisupport-address.md). 
  
La boîte de dialogue modale est un affichage en lecture/écriture d'entrées provenant d'un ou de plusieurs conteneurs. Son contenu peut être affecté de la même manière que la version non modale par restrictions définies dans les membres **lpContRestriction** et **lpHierRestriction** . En plus de la zone de liste affichant les entrées de conteneur, la boîte de dialogue modale peut contenir entre un et trois contrôles de zone de texte pour contenir les entrées sélectionnées par l'utilisateur. Chaque contrôle d'édition est associé à un type de destinataire particulier ou à une propriété **PR_RECIPIENT_TYPE** , telle que MAPI_TO. La boîte de dialogue d'adresses modale peut être affichée par l'une des méthodes d' **adresse** ou lorsque les clients appellent [IAddrBook::D etails](iaddrbook-details.md) et fournisseurs de services [IMAPISupport::D etails](imapisupport-details.md). 
  
Cette illustration comprend deux contrôles de zone de texte, car le membre **cDestFields** de la structure **ADRPARM** qui contrôle l'affichage de cette boîte de dialogue est défini sur 2. Le premier contrôle a le focus initial, car le membre **nDestFieldFocus** est défini sur 0. 
  
Le membre **lpszNewEntryTitle** pointe vers Text pour une étiquette de bouton qui, lorsqu'elle est sélectionnée, entraîne l'affichage d'une boîte de dialogue supplémentaire. En règle générale, comme indiqué dans l'illustration de la boîte de dialogue modale, le bouton est intitulé **nouveau** et la boîte de dialogue qui apparaît répertorie tous les types d'adresses qui peuvent être créés par l'un des fournisseurs de carnet d'adresses dans le profil. Les clients entraînent l'affichage de cette nouvelle boîte de dialogue d' **entrée** en appelant [IAddrBook:: NewEntry](iaddrbook-newentry.md) et en transmettant zéro pour le paramètre _cbEidNewEntryTpl_ et null pour le paramètre _lpEidNewEntryTpl_ lorsque l'utilisateur sélectionne le bouton. Les informations qui sont incluses dans cette boîte de dialogue proviennent de la table ponctuelle MAPI. 
  
Chaque entrée de cette boîte de dialogue est associée à un modèle pour entrer les données nécessaires à la création d'une adresse de type particulier. La plupart des fournisseurs de carnet d'adresses fournissent un modèle pour chaque type d'entrée d'adresse qu'ils peuvent créer. Lorsqu'un utilisateur effectue une sélection dans cette boîte de dialogue, MAPI affiche le modèle correspondant.
  
Les quatre bits les plus significatifs du membre **ulFlags** de la structure **ADRPARM** contiennent un numéro de version qui identifie la version de la structure **ADRPARM** . La version actuelle est 0 (zéro) ou ADRPARM_HELP_CTX. L'implémentation actuelle de MAPI échouera pour toutes les versions de la structure autres que zéro. 
  
Les versions ultérieures de la structure peuvent être complètement différentes; ils ne prennent pas en charge la structure de version zéro. Les macros suivantes sont fournies pour extraire le numéro de version du membre **ulFlags** et pour le combiner aux indicateurs définis: 
  
- **GET_ADRPARM_VERSION** (_ulFlags_) 
- **SET_ADRPARM_VERSION** (_ulFlags_, _ ulVersion _) 
- **ADRPARM_HELP_CTX**
  
## <a name="see-also"></a>Voir aussi

- [ACCELERATEABSDI](accelerateabsdi.md)
- [DISMISSMODELESS](dismissmodeless.md)
- [IAddrBook::Address](iaddrbook-address.md)
- [IMAPISupport::Address](imapisupport-address.md)
- [SRestriction](srestriction.md)
- [Structures MAPI](mapi-structures.md)

