RFC 4180 compliant PHP library for reading CSV files because PHP's
fgetcsv() does not comply to RFC 4180

Copied from Drupal Ubercart Stock & Price CSV Updater module.
http://www.ubercart.org/project/uc_stock_update-2x.

Example:

  $csv_reader = new ReadCSV( $file_handle, ',', "\xEF\xBB\xBF" ); // Skip any UTF-8 byte order mark.
  while ( ( $line = $csv_reader->get_row() ) !== NULL ) {
    var_dump( $line );
  }

