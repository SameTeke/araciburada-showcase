# Aracı Burada

Aracı Burada is a Turkish vehicle marketplace I developed through SCT Ajans. Sellers describe their car in a guided form, staff manage submissions and inventory, and buyers browse published listings. [See the site and interface walkthrough at SCT Ajans](https://sctajans.com/referanslar/araciburada/).

## The seller's journey

A seller starts with the model year, brand and model. The form narrows the available choices as the vehicle is identified. The remaining steps collect body condition, photos, colour and listing details, then location. The site also has separate entry points for motorcycles and consignment requests.

## The buyer's view

Staff manage listings and attach images in an administration panel. The public catalogue queries published listings, orders them by creation date and includes the images attached to each vehicle. Buyers can open a detail page for an individual listing. Seller submissions and public listings have separate database records, so sending an enquiry and publishing a vehicle are distinct actions.

## Implementation

- **Next.js and TypeScript** serve the seller form, public catalogue, vehicle detail pages and administration screens.
- **Prisma and PostgreSQL** model vehicle categories, makes, models and trims, along with form submissions, listings and their images.
- **Listing photos** are uploaded through an authenticated administration route and linked to their listing by ID.

## Read the listing code

The public source from the earlier release shows how the marketplace works under the hood. Follow a listing from the [staff creation handler](https://github.com/SameTeke/otosipsak/blob/main/src/app/api/admin/listings/route.ts) to the [published inventory query](https://github.com/SameTeke/otosipsak/blob/main/src/app/api/listings/route.ts). The current Aracı Burada application passed a local TypeScript check.
